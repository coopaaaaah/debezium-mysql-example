
Extracted from Full Tutorial here
https://debezium.io/documentation/reference/stable/tutorial.html

### Prereq
1. Have Docker installed and running
2. Have a halfway decent machine (4GB of RAM, 20GB of storage available)

### Startup Steps
1. docker compose up -d zookeeper kafka mysql_source connector
2. (inside connect container) curl -i -X POST -H "Accept:application/json" -H "Content-Type:application/json" localhost:8083/connectors/ --data-binary "@connector-config.json"
3. docker compose up -d watcher

