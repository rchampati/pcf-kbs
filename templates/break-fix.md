
#Break Fix Template (Add the Product name here)

##Environment

Populate the table with the environment specifications where the problem occurred as shown the example below. 

Product | Version
------- | --------
Pivotal Greenplum | (GPDB)	4.3.x
OS | RHEL 6.x
	 
##Symptom

Include a description of the symptoms or problem statement as shown in the example below:

When attempting an upgrade from XYZ version 1.2.2 to version 1.2.3, the installation fails with error message “Upgrade failed”.

Error Message:
If applicable, copy and paste the error message.
Note: These log entries use a volume named 12345678-abcdefg0 as an example:

`YYYY-04-01T14:35:08.074Z: [APDCorrelator] 9413898746us: [vob.storage.apd.start] Device or filesystem with identifier [12345678-abcdefg0] has entered the All Paths Down state.
YYYY-04-01T14:35:08.075Z: [APDCorrelator] 9414268686us: [esx.problem.storage.apd.start] Device or filesystem with identifier [12345678-abcdefg0] has entered the All Paths Down state.
YYYY-04-01T14:36:55.274Z: No correlator for vob.vmfs.nfs.server.disconnect
YYYY-04-01T14:36:55.274Z: [vmfsCorrelator] 9521467867us: [esx.problem.vmfs.nfs.server.disconnect] 192.168.1.1/NFS-DS1 12345678-abcdefg0-0000-000000000000 NFS-DS1
YYYY-04-01T14:37:28.081Z: [APDCorrelator] 9553899639us: [vob.storage.apd.timeout] Device or filesystem with identifier [12345678-abcdefg0] has entered the All Paths Down Timeout state after being in the All Paths Down state for 140 seconds. I/Os will now be fast failed.
YYYY-04-01T14:37:28.081Z: [APDCorrelator] 9554275221us: [esx.problem.storage.apd.timeout] Device or filesystem with identifier [12345678-abcdefg0] has entered the All Paths Down Timeout state after being in the All Paths Down state for 140 seconds. I/Os will now be fast failed` 

##Cause (Recommended if known)

Include a description of what caused the problem.  

###RCA (Optional, if applicable)

If the RCA is applicable, write the description.

While upgrading the XYZ version 1.2.2 to version 1.2.3, the backup intermittently stops working because of the following reasons:

*	Bullet List
*	Bullet List
*	Bullet List
*	Bullet List

##Resolution

Use any of the examples below to write the steps to resolve the problem.

Follow the steps to resolve this issue:

1.	Numbered List
2.	Numbered List
3.	Numbered List

Note: If you are unable to upgrade, using the instruction below try the following steps manually:

1.	Numbered List
2.	Numbered List
3.	Numbered List

##Additional Information (Optional)

Include additional information such as KB articles, references to the original documentation (e.g. Admin Guide or Installation Guide) or any other resource that helped documenting this article. 

###Internal Comments

Section: Include the section that you would like your article to be published in.

Notes: Provide any notes that you have for the SME or technical writer.


