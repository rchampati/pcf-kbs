![Loggregator Diagram](https://github.com/cloudfoundry/loggregator/blob/develop/docs/loggregator.png )

1. App Container
  2. App Instance (N)
  3. Logs 
2. Diego Executioner
  3. Metreon Agent
  4. Logs
4. Diego
  5. StatsD Metrics
    6. StatsD Injector
    7. Metron Agent
  8. Logs
