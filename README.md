> Hop Community data in Neo4j

# Load Hop Community information to Neo4j

Apache Hop (Incubating) has a very active community of users and contributors.

This repository collects a variety of Hop community sources into a Neo4j database. 

Sources that are currently available: 
* Mattermost messages 
* JIRA cases 

Sources that will be added in future releases: 
* git source code analysis
* downloads and website visits
* Twitter: direct messages, mentions, Hop-related hashtags 

TODO: 
* additional Mattermost data to include:  
  * url parsing
  * image parsing
  * threads 
* additional JIRA data to include:
  * users
  * issue history: updates, comments, ...   


# Loading the Hop community data to your Neo4j database 

Clone the repository: 

<code>git clone https://github.com/knowbi/knowbi-hop-community.git</code>

Copy `project-config.json.template` to `project-config.json` and change the variables (in the file or through Hop Gui): 

* login_id: your mattermost login id 
* password: your mattermost password
* mattermost_url: the default (https://chat.project-hop.org) should be fine 
* NEO4J_DB_HOST: Neo4j hostname or ip address
* NEO4J_DB_NAME: (default: neo4j) Neo4j database name. Only required for Neo4j EE  
* NEO4J_BOLT_PORT: (default: 7687)
* NEO4J_BROWSER_PORT: (default: 7474)
* NEO4J_USER: (default: neo4j)  
* NEO4J_PASS: your Neo4j password

The ASF's JIRA for Hop is publicly available, no authentication is required. 

Run `wf_community_main.hwf` to load the Hop community graph to your local Neo4j database. 