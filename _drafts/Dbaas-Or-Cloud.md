### Gold images and cloning
For those of you with auditors to answer to you will find that creating a gold image of the Oracle home and copying this to your instances will mean extra work to prove when the work was done
OPatch will show the patch date of the source not when the work was done on the target.  To get the date the container was patched you have to query DBA_REGISTRY_SQLPATCH and then explain the difference to your auditor friends

## Enterprise and Database as a service
Melvin Conway, who introduced this idea in 1967. His original wording was:

> organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations.
[M. Conway](http://www.melconway.com/Home/Conways_Law.html)

Or
> Any organization that designs a system [...] will inevitably produce a design whose structure is a copy of the organization's communication structure."

[Is this your shared service](https://www.smh.com.au/public-service/government-abandons-210-million-shared-services-white-elephant-20170524-gwc0u6.html)
or [this](https://www.pinsentmasons.com/out-law/news/uk-government-it-to-be-consolidated-as-part-of-new-shared-services-drive)
This is seen in these pain points:
- Database staff don't have root access on servers  (segregation of duties)
- What you say!  Cannot install Oracle without root so then you get the back and forth over limited permissions to run as root
- Database staff have no control over backups and limited control over restores
- but there are numerous ways to get root access so it's hard to rule it out when something goes wrong
- Client DBA's don't have sys access on databases (more segregation of duties)
- yet it is still possible to  create datafiles in another client's tablespace
-


## Upgrading - You're not done yet?
- Very common after consulting firms have come and gone to see application managers controlling the budget for their applications which is all fine and good.  It starts to hurt when the database as a service team says it's time to upgrade the database so you need to upgrade how your application connects to the database. Sometimes there is no money or there are no resources or there is no interest.  It's working so why upgrade?


## Why AWS won't be a silver bullet for Government
- AWS has a core idea that authority should be pushed down to developers so they can innovate.
- Let a developer spin up a server where they can set the root password, set routing?  Security won't want to buy in, managers will see unexplained bills that could come in
- some government workloads do scale up: think tax submission time, end of month cycles, outward facing websites with current information.  For these use cases the ability to scale workload as required can reduce costs. Many other applications have a workload that grows over extended period or gets really busy at night when the data warehouse gets busy doing ETL.
- working with AWS also implies that some jobs change, some are not required and there are new jobs. This won't sit well with a heavily unionized workface that is used to jobs not changing at all.
- all these issues can be addressed on the technical side with existing tools Amazon supplies like security templates but social factors are much more difficult

- Amazon offers RDS which supplies:
  - server maintenance
  - software install and patching
  - database backups and high availability
  - data security
  - capacity scaling
  - OS install and patching
  
  Note: no containers for RDS
  pick your own storage type and size
  VPC provides segmented network by design
  built in standby and automatic failover
  
Overall I imagine the reaction will be to try and duplicate the existing infrastructure in the cloud and optimize later, if at all.

Even agencies that want to go to the cloud can find unexpected costs see
[here](https://www.theregister.co.uk/2020/03/19/nasa_cloud_data_migration_mess/)


# What they say and what they hear
Here's the official plan of the Government of Canada courtesy of [Treasury Board Secretariat](https://www.canada.ca/en/treasury-board-secretariat/services/information-technology/strategic-plan-2017-2021.html#toc15)
![Government of Canada Strategic Plan](/images/GCStrategicPlan.jpg "Government of Canada Strategic Plan")
> Use common government solutions and platforms. Build cloud first

> blah, blah, blah, Cloud, blah, blah, Cloud, blah, blah, Cloud


![What we say, what they hear](/images/whatWeSay.jpg "Courtesy of Gary Larson")

# Outsourcing and near shoring
see [this](https://www.troyhunt.com/offshoring-roulette-lessons-from-outsourcing-to-india-china-and-the-philippines/) for thoughts 
and that famous quote  
> They're just not thought leaders

  
