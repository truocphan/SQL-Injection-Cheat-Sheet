# SQL-Injection-Cheat-Sheet

## MySQL
`SELECT @@hostname;`

`SELECT version();`
`SELECT @@version;`

`SELECT user();`
`SELECT system_user();`

#Current database
`SELECT database();`

#Get Database name
`SELECT schema_name FROM information_schema.schemata;
SELECT distinct(table_schema) FROM information_schema.tables;
SELECT distinct(table_schema) FROM information_schema.columns;
SELECT name FROM information_schema.innodb_tables;
SELECT name FROM information_schema.innodb_tablestats;
SELECT distinct(table_schema) FROM information_schema.key_column_usage;
SELECT distinct(table_schema) FROM information_schema.partitions;
SELECT distinct(table_schema) FROM information_schema.statistics;
SELECT distinct(db) FROM mysql.db;
SELECT distinct(database_name) FROM mysql.innodb_index_stats;
SELECT distinct(database_name) FROM mysql.innodb_table_stats;
SELECT distinct(table_schema) FROM sys.schema_index_statistics;
SELECT distinct(db) FROM sys.schema_object_overview;
SELECT distinct(table_schema) FROM sys.schema_table_statistics;
SELECT distinct(table_schema) FROM sys.x$schema_index_statistics;
SELECT distinct(table_schema) FROM sys.x$schema_table_statistics;`

#Get Table name
`SELECT table_name FROM information_schema.tables;
SELECT table_name FROM mysql.innodb_table_stats;
SELECT table_id,name FROM information_schema.innodb_columns;
SELECT name FROM information_schema.innodb_tables;
SELECT name FROM information_schema.innodb_tablestats;
SELECT table_name FROM information_schema.key_column_usage WHERE table_schema="{DATABASE_NAME}";
SELECT table_name FROM information_schema.partitions WHERE table_schema="{DATABASE_NAME}";
SELECT table_name FROM information_schema.statistics WHERE table_schema="{DATABASE_NAME}";
SELECT distinct(table_name) FROM mysql.innodb_index_stats WHERE database_name="DATABASE_NAME";
SELECT distinct(table_name) FROM mysql.innodb_table_stats WHERE database_name="DATABASE_NAME";
SELECT distinct(table_name) FROM sys.schema_index_statistics WHERE table_schema="{DATABASE_NAME}";
SELECT distinct(table_name) FROM sys.schema_table_statistics WHERE table_schema="{DATABASE_NAME}";
SELECT distinct(table_name) FROM sys.x$schema_index_statistics WHERE table_schema="{DATABASE_NAME}";
SELECT distinct(table_name) FROM sys.x$schema_table_statistics WHERE table_schema="{DATABASE_NAME}";`

#Get Column name
`SELECT column_name FROM information_schema.columns WHERE table_schema="{DATABASE_NAME}" AND table_name="{TABLE_NAME}";
SELECT column_name FROM information_schema.key_column_usage WHERE table_schema="{DATABASE_NAME}" AND table_name="{TABLE_NAME}";
SELECT column_name FROM information_schema.statistics WHERE table_schema="{DATABASE_NAME}" AND table_name="{TABLE_NAME}";`
