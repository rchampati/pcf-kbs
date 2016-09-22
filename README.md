Knowledge Base Guide
===========

-   [Getting Started](https://github.com/timani/pcf-loggregator/tree/structure#overview)
 -   [Setting up your board](https://github.com/timani/pcf-loggregator/tree/structure#playbooks)
-   [Roles](https://github.com/timani/pcf-loggregator/tree/structure#general)
    - [Knowledge Management](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)
    - [Subject Matter Expert](https://github.com/cloudfoundry/docs-cf-cli)
    - [GSS Contributor](http://github.com/cloudfoundry/docs-dev-guide)
-   [Workflow](https://github.com/timani/pcf-loggregator/tree/structure#general)
    - [Adding stories](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)
    - [Updating stories](https://github.com/cloudfoundry/docs-cf-cli)
    - [Review process](http://github.com/cloudfoundry/docs-dev-guide)    
-   [Resources](https://github.com/timani/pcf-loggregator/tree/structure#general) 
    - [Tracker](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)
    - [Bookmarks & Links](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)



Overview
------------------

Loggregator is composed of Doppler**: Responsible for gathering logs from the **Metron agents**, storing them in temporary buffers, and forwarding logs to 3rd party syslog drains.

Playbooks
-----------------

### General

* [Installation](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)
* [Upgrade](https://github.com/cloudfoundry/docs-cf-cli)
* [Data Loss](http://github.com/cloudfoundry/docs-dev-guide)
* [Performance](http://github.com/cloudfoundry/docs-dev-guide)
 
### Components

* [Sources](https://github.com/) - Logging agents that run on the Cloud Foundry components.[Runner VMs](https://github.com/)
* [Metron](https://github.com/) - Metron agents are co-located with sources. They collect logs and forward them to
* [Cloud Controller VMs](https://github.com/)
 * [Cloud Controller](https://github.com/)
 * [Go Router](https://github.com/)
 * [UAA](https://github.com/)
* [Doppler](https://github.com/) - Responsible for gathering logs from the **Metron agents**, storing them in temporary buffers, and forwarding logs to 3rd party syslog drains
* [Traffic Controller](https://github.com/) - Handles client requests for logs. Gathers and collates messages from all Doppler servers, and provides external API and message translation (as needed for legacy APIs).
* [Nozzles](https://github.com/)

Training Guide
---------------------------

* [Gettings Started](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)
* [Overview of the Loggregator System](https://github.com/cloudfoundry/docs-cf-cli)
* [Application Logging in Cloud Foundry](http://github.com/cloudfoundry/docs-dev-guide)
* [Component Metrics](http://github.com/cloudfoundry/docs-deploying-cf)
* [Nozzles and Firehose](http://github.com/cloudfoundry/docs-running-cf)

Resources
------------------------------ 

* [Webinars & Videos](http://github.com/cloudfoundry/docs-cloudfoundry-concepts)
* [Documentation](https://github.com/cloudfoundry/docs-cf-cli)
* [Articles](http://github.com/cloudfoundry/docs-dev-guide) 
* [Glossary](http://github.com/cloudfoundry/docs-dev-guide)

  
### Contributing

Read [CONTRIBUTING.md](<CONTRIBUTING.md>) for more details on contributing
documentation improvements.

