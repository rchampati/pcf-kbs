### Log loss 
----------

- Check environment 
  - Verify etcd cluster health
  - verify multi zone access
    - how many dopplers does traffic controller see?
- Look for patterns
  - Losses correlated to:
  - App events/crashes
  - regular time interval
    - look at doppler to Diego cell ratio, target config ratio of......
    - control plane updates (deployments)
- Isolate loss
  - Are the counts of messages from Diego to Metron adding up?
  - Are the count of metron to Doppler adding up
  - If config is using UDP as transport protocol, consider adding more dopplers to accommodate burst......
