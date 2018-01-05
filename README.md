Roadmap for the 🍡**kdango** project.

In this moment, the aim is to build a simple POC of three most important kdango parts: manager, database and CPM.

# Manager

The Manager is one of the most important part of the kdango. It needs to orchestrate all communications between the crawlers.

* [ ] Explore some message broker to use in the project (for example, RabbitMQ)
* [ ] Create a poc of communication between the manager and crawlers
* [ ] The manager needs start a crawlers and obtain the data collected by it

# Database

Is important organize the kdango database to store and retrieve the informations collected.
Probably, the best database to use in this project project is some graph-oriented databsae (like neo4j and dgraph).

* [ ] An indepedent crawler needs collected informations and store in graph-oriented database 
* [ ] A dependent crawler needs retrieve informations from a database and store new informations

# Crawlers Package Manager (CPM)

The CPM is the tool where the user can install a new crawler in system.
Since each crawler is a microservice, the CPM needs create a new instance of each crawler, accessible by the Manager.

The crawlers also be versionable, then one feature of the CPM is update a crawlers.

* [ ] Create a new instance in some IaaS automaticlly
* [ ] Use some configuration file (`.yaml`, `.json` or `.toml`) to create the instance of crawlers
* [ ] The CPM needs check the changes in the configuration file to update the crawler's instances (for example, if a crawler was removed)
