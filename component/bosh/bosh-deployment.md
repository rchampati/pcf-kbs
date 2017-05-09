---
title: Name of the article
template: Break-fix
id: 115006886227
locale: en-us
---

Srikanth Manvi [11:10 AM] 
Can anyone let me know how to set `bosh deployment` to a service instance ? or where are the yml files related to service instances located ?
```ubuntu@pivotal-ops-manager:/var/tempest/workspaces/default/deployments$ bosh deployment service-instance_68c105a1-ef7f-4400-9c84-2c74d09fa50b
Missing manifest for 'service-instance_68c105a1-ef7f-4400-9c84-2c74d09fa50b'
```

Daniel Mikusa [11:23 AM] 
That’s a trick question :slightly_smiling_face:  The yml files don’t exist anywhere for on-demand bosh deployed service instances.

[11:23] 
At least not on the service broker.

[11:23] 
I believe they’re stored in memory, unless something has changed there

[11:24] 
What you can do is run `bosh download manifest <deployment-name> <filename>`.

[11:24] 
and Bosh should download the manifest for you.

[11:25] 
There are some failure cases where this does not happen though, i.e. if the deployment fails early enough.  Bosh will just download a blank file.

[11:25] 
In that case, I think you’d want to look at the service broker’s logs to see what’s happening.

[11:25] 
Hope that helps!

Srikanth Manvi [11:25 AM] 
ok good to know.. yes that helps..

[11:26] 
