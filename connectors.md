This is a document of connectors that can be used to connect to MariaDB:

Connector | License | Features | MariaDB Support | Source | Issues | CI
---|---|---|---|---|---|---
[MariaDB Connector/C (and C++)](https://mariadb.com/kb/en/mariadb-connector-c/) | LGPL-2.1-only | Conn(all, [proxy](https://mariadb.com/kb/en/proxy-protocol-support/#client-side-support-for-proxy-protocol)), auth(default, [extra](https://mariadb.com/kb/en/mysql_optionsv/#plugin-options), [custom via MYSQL_PLUGIN_DIR](https://mariadb.com/kb/en/mysql_optionsv/#plugin-options)), [prep](https://mariadb.com/kb/en/mariadb-connectorc-api-prepared-statement-functions/), ok(default,status), [rep](https://github.com/mariadb-corporation/mariadb-connector-c/wiki/binlog_api) | All Versions | [source](https://github.com/mariadb-corporation/mariadb-connector-c) | [JIRA](https://jira.mariadb.org/issues/?jql=project%3DCONC%20and%20status!%3DClosed) | [GH Actions](https://github.com/mariadb-corporation/mariadb-connector-c/actions), [Travis CI](https://app.travis-ci.com/github/mariadb-corporation/mariadb-connector-c)
[MariaDB Connector/Node.js](https://mariadb.com/kb/en/nodejs-connector/) |  LGPL-2.1-only | Promise + Callback | All Versions | [source](https://github.com/mariadb-corporation/mariadb-connector-nodejs) | [JIRA](https://jira.mariadb.org/issues/?jql=project%3DCONJS%20and%20status!%3DClosed) | [Travis CI](https://app.travis-ci.com/github/mariadb-corporation/mariadb-connector-nodejs)

* MariaDB Connector/ODBC
* MariaDB Connector/J
* MariaDB Connector/Python
* MariaDB Connector/R2DBC
* MySqlConnector for ADO.NET
* ADO.NET Driver for MySQL (Connector/NET)
* ODBC Driver for MySQL (Connector/ODBC)
* JDBC Driver for MySQL (Connector/J)
* Node.js Driver for MySQL (Connector/Node.js)
* C++ Driver for MySQL (Connector/C++)
* C Driver for MySQL (Connector/C)
* C API for MySQL (mysqlclient)
* PyMySQL
* mysql-python

Features of connectors:

Feature Abbreviation | Class | Set | Extra
---|---|---|---
Conn | Connections | tcp, socket, npipe, shm | [proxy](https://mariadb.com/kb/en/proxy-protocol-support/)
Auth | Auth plugins | default - mysql_native_password, extra += dialog, client_ed25519, caching_sha2_password, sha256_password, auth_gssapi_client, mysql_old_password, mysql_clear_password | custom - user defined
cap | [Capabilities](https://mariadb.com/kb/en/connection/#capabilities) | mysql - (all before CLIENT_REMEMBER_OPTIONS), progress = MARIADB_CLIENT_PROGRESS, multi - MARIADB_CLIENT_COM_MULTI, bulk - MARIADB_CLIENT_STMT_BULK_OPERATIONS, extendtype = MARIADB_CLIENT_EXTENDED_TYPE_INFO, cachemeta = MARIADB_CLIENT_CACHE_METADATA
prep | Prepared statements |
loaddatalocal | Load Data Local | file, programaticly
ok | [OK Packet contents](https://mariadb.com/kb/en/ok_packet/) | default - rows, last insert, status += server status, warncount, info, sessionstate`
rep | [Replication Data](https://mariadb.com/kb/en/replication-protocol/) | basic, semisync += semisync
