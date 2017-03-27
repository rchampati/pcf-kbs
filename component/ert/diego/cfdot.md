---
title: How to use CF Diego Operator Toolkit
template: how-to
id: 
locale: en-us
---

# How to use CF Diego Operator Toolkit

**Environment**

Pivotal Cloud Foundry

**Purpose**

This topic provides instructions for installing and using the `cfdot` command-line interface (CLI) tool to interact with Diego components in your Pivotal Cloud Foundry (PCF) deployment.

This CLI tool uses stateless execution to provide information about the Diego cells in your deployment. `cfdot` outputs a stream of JSON values that you can process with `jq`, `bash`, and other line-based UNIX tools.

**Prerequisites**

To use the `cfdot` command-line tool, you must either:

* install [`cfdot`](https://github.com/cloudfoundry/cfdot) alongside a running Diego deployment, or
* generate your Diego manifest using the [generate-deployment-manifest script](https://github.com/cloudfoundry/diego-release/blob/master/scripts/generate-deployment-manifest).

**Installation**

1. Enter the following command to run the `setup` script:

    ```
    $ bosh ssh <DIEGO_JOB>/<INDEX>
    $ source /var/vcap/jobs/cfdot/bin/setup
    ```

    The `setup` script does three things:

      * Exports environment variables to target the BBS API in the deployment
      * Puts the `cfdot` binary on the `PATH`
      * Puts a `jq` binary on the `PATH`

2. Perform the following step from a GOPATH to install the Diego BBS client library. For example, from the `diego-release` directory, run the following commands:

    ```
    $ go get code.cloudfoundry.org/cfdot
    $ cd src/code.cloudfoundry.org/cfdot
    ```

3. Build `cfdot` by running the command that corresponds to your operating system:

    | If your OS is...   | then enter...               |
    |--------------------|-----------------------------|
    | Mac                | `$ GOOS=darwin go build .`  |
    | Linux              | `$ GOOS=linux go build .`   |
    | Windows            | `$ GOOS=windows go build .` |

**cfdot Command Examples**

Use `cfdot` to make requests to Diego using the BBS API.

* To count the total number of desired app instances, enter the following command:

  ```
  $ cfdot desired-lrp-scheduling-infos | jq '.instances' | jq -s 'add'
  ```

This command outputs a number, such as `568`.

* To show the instance counts of all apps by state, enter the following command:

  ```
  $ cfdot actual-lrp-groups | jq '.instance, .evacuating | values' | jq -s -r 'group_by(.state)[] | .[0].state + ": " + (length | tostring)'
  ```

  This command outputs a list of app states and the number of apps that are currently in those states. For example:

    ```
    CRASHED: 36
    RUNNING: 531
    UNCLAIMED: 1
    ```

* Other supported `cfdot` commands are listed below:

  ```
  $ cfdot --help
  A command-line tool to interact with a Cloud Foundry Diego deployment

  Usage:
    cfdot [command]

  Available Commands:
    actual-lrp-groups            List actual LRP groups
    actual-lrp-groups-for-guid   List actual LRP groups for a process guid
    create-desired-lrp           Create a desired LRP
    delete-desired-lrp           Delete a desired LRP
    delete-task                  Delete a Task
    desired-lrp                  Show the specified desired LRP
    desired-lrp-scheduling-infos List desired LRP scheduling infos
    desired-lrps                 List desired LRPs
    domains                      List domains
    retire-actual-lrp            Retire actual LRP by index and process guid
    set-domain                   Set domain
    task                         Display task
    update-desired-lrp           Update a desired LRP

  Use "cfdot [command] --help" for more information about a command.
  ```