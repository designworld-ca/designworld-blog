### Gold images and cloning
For those of you with auditors to answer to you will find that creating a gold image of the Oracle home and copying this to your instances will mean extra work to prove when the work was done
OPatch will show the patch date of the source not when the work was done on the target.  To get the date the container was patched you have to query DBA_REGISTRY_SQLPATCH and then explain the difference to your auditor friends

## Enterprise and Database as a service
Melvin Conway, who introduced this idea in 1967. His original wording was:

> organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations.

This is seen in these pain points:
- Database staff don't have root access on servers  (segregation of duties)
- but there are numerous ways to get root access so it's hard to rule it out when something goes wrong
- Client DBA's don't have sys access on databases (more segregation of duties)
- yet it is still possible to  create datafiles in another client's tablespace
-


## Upgrading - You're not done yet?
- Very common after consulting firms have come and gone to see application managers controlling the budget for their applications which is all fine and good.  It starts to hurt when the database as a service team says it's time to upgrade so you need to upgrade how your application connects to the database. Sometimes there is no money or there are no resources or there is no interest.  It's working so why upgrade?
— M. Conway[2](http://www.melconway.com/Home/Conways_Law.html)
