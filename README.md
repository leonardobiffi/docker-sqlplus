## SQL*Plus Docker image

Connect to a running Oracle database like this

`docker run --interactive guywithnose/sqlplus sqlplus user/password@hostname:port/service_name`

Or run your own Oracle XE database through docker and then connect to it.

```bash
docker run --detach --name myOracle guywithnose/oracle-xe-11g
(Wait for Oracle to initialize)
docker run --interactive --link myOracle:oracle guywithnose/sqlplus
```
