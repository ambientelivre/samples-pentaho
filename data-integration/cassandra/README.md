# This small project is a test stress for cassandra by PDI
have two transformations: one load te database and other read database. Use step metrics of PDI for analize. 


## Config Cassandra PDI Stress

### Create a KeySpace in Cassandra

CREATE KEYSPACE hackcassandra WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1 } ;

### Create a Column Family em Cassandra (Table)
CREATE TABLE temperatura_by_day (
  weatherstation_id text,
  date text,
  event_time timestamp,
  temperatura text,
 PRIMARY KEY ((weatherstation_id,date),event_time)
);

This transformation connection is config for cassandra in localhost (alter ip or dns for your configs cassandra)
