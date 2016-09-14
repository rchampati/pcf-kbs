Loggregator Handbook
===========

-   [Guide](https://github.com/)
-   [Components](https://github.com/)
-   [Dependencies](https://github.com/)
-   [Contributing](https://sculpin.io/)

### Overview

Loggregator is composed of:
* **Sources**: Logging agents that run on the Cloud Foundry components.
* **Metron**: Metron agents are co-located with sources. They collect logs and forward them to:
* **Doppler**: Responsible for gathering logs from the **Metron agents**, storing them in temporary buffers, and forwarding logs to 3rd party syslog drains.
* **Traffic Controller**: Handles client requests for logs. Gathers and collates messages from all Doppler servers, and provides external API and message translation (as needed for legacy APIs).

![Loggregator Diagram](https://github.com/cloudfoundry/loggregator/blob/develop/docs/loggregator.png )

### Guides
* [Cloud Foundry Concepts](http://github.com/cloudfoundry/docs-cloudfoundry-concepts): Underlying concepts and architecture
* [Cloud Foundry Command-Line Interface (cf CLI)](https://github.com/cloudfoundry/docs-cf-cli): A guide to the cf CLI for Cloud Foundry developers and users 
* [Developer Guide](http://github.com/cloudfoundry/docs-dev-guide): Step-by-step instructions and reference material for developers pushing applications to Cloud Foundry
* [Deploying Cloud Foundry](http://github.com/cloudfoundry/docs-deploying-cf): Instructions for operators using BOSH to deploying Cloud Foundry on AWS, vSphere, vCloud, OpenStack, etc.
* [Running Cloud Foundry](http://github.com/cloudfoundry/docs-running-cf): Information for operators running Cloud Foundry
* [Administrator Tools](https://github.com/cloudfoundry/docs-cf-admin): Documentation about operating Cloud Foundry deployments using BOSH and the cf command line tool

### Components
Source agents emit the logging data as [protocol-buffers](https://github.com/google/protobuf), and the data stays in that format throughout the system.

1. [Runner VMs](https://github.com/)
1. [Cloud Controller VMs](https://github.com/)
2. [Doppler](https://github.com/)
3. [Traffic Controller](https://github.com/)
4. [Nozzles](https://github.com/)

On AWS, availability zones could be used as redundancy zones. The following is an example of a multi zone setup with two zones.

### Playbooks
* [Cloud Foundry Concepts](http://github.com/cloudfoundry/docs-cloudfoundry-concepts): Underlying concepts and architecture
* [Cloud Foundry Command-Line Interface (cf CLI)](https://github.com/cloudfoundry/docs-cf-cli): A guide to the cf CLI for Cloud Foundry developers and users 
* [Developer Guide](http://github.com/cloudfoundry/docs-dev-guide): Step-by-step instructions and reference material for developers pushing applications to Cloud Foundry
* [Deploying Cloud Foundry](http://github.com/cloudfoundry/docs-deploying-cf): Instructions for operators using BOSH to deploying Cloud Foundry on AWS, vSphere, vCloud, OpenStack, etc.
* [Running Cloud Foundry](http://github.com/cloudfoundry/docs-running-cf): Information for operators running Cloud Foundry
* [Administrator Tools](https://github.com/cloudfoundry/docs-cf-admin): Documentation about operating Cloud Foundry deployments using BOSH and the cf command line tool

### Dependencies
The properties discussed below as well as their behavior might change in the future.

1. [etcd](https://github.com/)
1. [consul](https://github.com/)

### Direcory Structure

1. Clone your fork of the content repository. Make sure to clone your fork of the topic repository to a directory that is a sibling to this book repository. So, for example, if you are contributing content to the Buildpack documentation, your folder structure would look like this:

  <pre>
    +-- docs-book-cloudfoundry
    | +-- docs-buildpacks
    +-- docs-buildpacks
    | +-- docs-buildpacks
    | +-- docs-buildpacks
  </pre>


### Contributing

Read [CONTRIBUTING.md](<CONTRIBUTING.md>) for more details on contributing
documentation improvements.

