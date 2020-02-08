### Gold images and cloning
For those of you with auditors to answer to you will find that creating a gold image of the Oracle home and copying this to your instances will mean extra work to prove when the work was done
OPatch will show the patch date of the source not when the work was done on the target.  To get the real date you have to query DBA_REGISTRY_SQLPATCH for the real data and then explain the difference to your auditor friends
