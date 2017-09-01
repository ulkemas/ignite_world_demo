# Ignite World Database Usage Sample

The project uses a dump of the word database altered for Ignite DDL syntax and shows how to:

* Create SQL schema and preload data using prepared ignite_world.sql script.
* Process the loaded data using SQL queries.
* Process the loaded data using key-value operations.

## SQL Schema Creation and Data Preloading

Download Apache Ignite 2.1 or later version:
https://ignite.apache.org/download.cgi#binaries

Download SQLLine tool:
https://github.com/julianhyde/sqlline

Set up SQLLine doing the following:
1. Copy *{apache_ignite_version}/libs/ignite-core.jar* file to *{sqlline}/bin* directory.
2. Download *ignite_world.sql* from the root of this project and paste into *{sqlline}/bin* directory.

Connect to Ignite cluster and execute the SQL script:
1. Start one or multiple cluster nodes using *{apache_ignite_version}/bin/ignite.sh* shell script (use ignite.bat for
Windows).
2. Connect to the cluster from SQLLine using this command:
*{sqlline}/bin/sqlline -d org.apache.ignite.IgniteJdbcThinDriver --color=true --verbose=true --showWarnings=true --showNestedErrs=true -u jdbc:ignite:thin://127.0.0.1/* (use sqlline.bat for Windows)
