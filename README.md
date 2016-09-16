Loggregator Handbook
===========

-   [Overview](https://github.com/)
-   [Components](https://github.com/)
-   [Dependencies](https://github.com/)
-   [Logs](https://github.com/)
-   [Training Guide](https://github.com/)
-   [Resources](https://github.com/)
-   [Glossary](https://github.com/)

Overview
------------------

Loggregator is composed of Doppler**: Responsible for gathering logs from the **Metron agents**, storing them in temporary buffers, and forwarding logs to 3rd party syslog drains.

Architecture
-----------------

![Loggregator Diagram](https://github.com/cloudfoundry/loggregator/blob/develop/docs/loggregator.png )

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
* [Doppler](https://github.com/) - Responsible for gathering logs from the **Metron agents**, storing them in temporary buffers, and forwarding logs to 3rd party syslog drains
* [Traffic Controller](https://github.com/) - Handles client requests for logs. Gathers and collates messages from all Doppler servers, and provides external API and message translation (as needed for legacy APIs).
* [Nozzles](https://github.com/)

### Dependencies
The properties discussed below as well as their behavior might change in the future.

1. [etcd](https://github.com/)
1. [consul](https://github.com/)
2. [syslog](https://github.com/)

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
* [Training](http://github.com/cloudfoundry/docs-dev-guide)
* [Glossary](http://github.com/cloudfoundry/docs-dev-guide)

  
### Contributing

Read [CONTRIBUTING.md](<CONTRIBUTING.md>) for more details on contributing
documentation improvements.

