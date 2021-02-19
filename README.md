## Requirements

- Docker: https://docs.docker.com/engine/install/
- Docker Compose: https://docs.docker.com/compose/install/

## Run

- docker-compose up -d

## Setup docker database oracle

- The database server is ready to use when the STATUS field shows (healthy) in the output of docker ps (WAIT A FEW MINUTES)
- The default password to connect to the database with sys user is Oradoc_db1.
- Obs:. Give permissions to the volume folder(data) if container qvc-db down and status exitted
- `docker login`
- `docker exec -it db-oracle bash`
- `sqlplus sys/Oradoc_db1@ORCLCDB as sysdba`
- `alter session set "_ORACLE_SCRIPT"=true;`
- `create user root identified by root;`
- `GRANT ALL PRIVILEGES TO root;`
- `exit;`

- If you have a database, access sqldeveloper to copy

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](https://mit-license.org/)**
- Quality 2020 © <a href="javascript:;" target="_blank">Quality</a>.
