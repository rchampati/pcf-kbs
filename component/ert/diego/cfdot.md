---
title: How to use cfdot to investigate Diego cells
template: how-to
id: 115004883487 
locale: en-us
---

**Environment**

Pivotal Cloud Foundry

**Purpose**

This topic provides instructions for installing and using the CF Diego Operator Toolkit (cfdot) Command Line Interface (CLI) tool to interact with Diego cells in your Pivotal Cloud Foundry (PCF) 1.10 deployment.

This CLI tool communicates directly with the Bulletin Board System (BBS) API to provide information about the Diego cells in your deployment.
The cfdot CLI outputs a stream of JSON values that you can process with `jq`, `bash`, and other line-based UNIX tools.

**Symptoms**

Use the cfdot CLI tool to investigate the following issues:

* Crashing apps
* Processes consuming too many resources
* Unknown app states

**Procedure**

1. SSH into the Diego cell:

    ```
    $ bosh ssh DIEGO_JOB/INDEX
    ```

    Replace the following items with values from your deployment:

    * DIEGO_JOB is the name of the Diego cell, such as `diego_brain` or `diego_cell`
    * INDEX is the number assigned to that particular VM

    For example, `$ bosh ssh diego_cell/0`

2. Enter the following command to run the `setup` script:

    ```
    $ source /var/vcap/jobs/cfdot/bin/setup
    ```

    The `setup` script does the following:

      * Exports environment variables to target the BBS API in your deployment
      * Puts the `cfdot` binary on the `PATH`
      * Puts a `jq` binary on the `PATH`

    Because Diego cells are frequently recreated in a typical deployment, you need to run the script each time you log into a Diego cell.

3. Run `cf dot --help` for the most current list of supported commands. The available commands include the following:
    * `actual-lrp-groups`: List actual LRP groups
    * `actual-lrp-groups-for-guid`:  List actual LRP groups for a process GUID
    * `create-desired-lrp`: Create a desired LRP
    * `delete-desired-lrp`: Delete a desired LRP
    * `delete-task`: Delete a Task
    * `desired-lrp`: Show the specified desired LRP
    * `desired-lrp-scheduling-infos`: List desired LRP scheduling infos
    * `desired-lrps`: List desired LRPs
    * `domains`: List domains
    * `retire-actual-lrp`: Retire actual LRP by index and process GUID
    * `set-domain`: Set domain
    * `task`: Display task
    * `update-desired-lrp`: Update a desired LRP

4. Enter one of the cfdot commands above. cfdot will print out all the information the BBS has about the tasks, LRPs, or groups you specified. You can pipe the output to `jq` or another line-based UNIX tool
to tailor your results or make them easier to read.

    * The following command displays every desired LRP in your deployment. The output includes the same information as `cfdot desired-lrp`, but prints in a more readable format:

    ```
    $ cfdot desired-lrp | jq .
    ```

    * The following command displays the information about a particular app by its GUID:

    ```
    $ cfdot desired-lrp GUID | jq .
    ```

    * The following command counts the total number of desired application instances:

    ```
    $ cfdot desired-lrp-scheduling-infos | jq '.instances' | jq -s 'add'
    ```

    * The following command shows the instance counts of all apps by state:

    ```
    $ cfdot actual-lrp-groups | jq '.instance, .evacuating | values' | jq -s -r 'group_by(.state)[] | .[0].state + ": " + (length | tostring)'
    ```
