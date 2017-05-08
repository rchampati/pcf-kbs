---
title: Stemcell 3363.20
template: Concepts
id: 115006975928 
locale: en-us
---

## Environment

Product	| Version
--------|---------
Stemcell|	3363.20

## Introduction 

Stemcell 3363.20, which has been published on PivNet, disables IPv6 at the kernel level.  This is not likely to impact your applications or services within your PCF foundations, but there is a small chance that it will.

## Description
Tiles provided by Pivotal or other vendors will be testing to verify that they are not negatively impacted by this.  Customers who are building their own tiles should be aware of this change and test for compatibility accordingly before pushing to production environments.  This stemcell is available on PivNet today to test against.  Customers enrolled in the Early Access Program can also test against alpha builds of Ops Manager for 1.11 which all include versions of the stemcell that include this change.

Some applications on the Elastic Runtime platform may also be impacted by this when deploying ERT with a stemcell that enables IPv6.  This is unlikely, but please refer to this article for further details.

There are at least 3 ways that network communication may occur between VMs within a PCF foundation:

Application instance (running on ERT) to a BOSH-deployed VMs.
Communication between BOSH-deployed VMs.  
Communication between a BOSH-deployed VM and off-board resources.

## Additional Information 
Note that IPv6 is currently not supported within the ERT, so any network connections that are made between application instances and their bound services will be initiated over IPv4.  Similarly for communication between BOSH-deployed VMs.  The third case is not necessarily constrained by ERT, and is the tile’s responsibility.  

As a matter of good security hygiene, and reducing the attack surface of a PCF foundation, it is important to not enable protocols or open ports that are not actually used or needed.  If a tile is binding to IPv6 interfaces unnecessarily, this must be disabled.  If you have an explicit requirement to support IPv6 in some way please let Pivotal know.


 
