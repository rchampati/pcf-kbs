Loggregator Handbook
===========

-   [Version-controlled](https://github.com/)
-   [Forkable](https://github.com/)
-   [Continuously updated](https://github.com/)
-   [Written in markdown](https://sculpin.io/)

Loggregator is composed of:
* **Sources**: Logging agents that run on the Cloud Foundry components.
* **Metron**: Metron agents are co-located with sources. They collect logs and forward them to:
* **Doppler**: Responsible for gathering logs from the **Metron agents**, storing them in temporary buffers, and forwarding logs to 3rd party syslog drains.
* **Traffic Controller**: Handles client requests for logs. Gathers and collates messages from all Doppler servers, and provides external API and message translation (as needed for legacy APIs).

![Loggregator Diagram](https://github.com/cloudfoundry/loggregator/blob/develop/docs/loggregator.png )

Source agents emit the logging data as [protocol-buffers](https://github.com/google/protobuf), and the data stays in that format throughout the system.

1. [Runner VMs](https://github.com/)
1. [Cloud Controller VMs](https://github.com/)
2. [Doppler](https://github.com/)
3. [Traffic Controller](https://github.com/)
4. [Nozzles](https://github.com/)

On AWS, availability zones could be used as redundancy zones. The following is an example of a multi zone setup with two zones.

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

