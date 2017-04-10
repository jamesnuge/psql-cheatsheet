# Nuge's PSQL Cheatsheet

## Package Installation

When installing a postgres instance from a package manager the password for the postgres user is not set. To login and update the password use the following commands

```
    sudo -u postgresql psql postgresql
    \password postgresql 
```

The first command will open psql as the postgresql user. The second command will then prompt you to enter a new password for the postgresql user

## Data Exporting

To export a database to a data file use the following command

```
    pg_backup -h ${HOST} -p ${PORT} -U ${USER_NAME} ${DB_NAME} > ${OUTPUT_FILE}
```

## Data Importing

To import a data file from an export use the following command

```
    pg_restore --verbose --clean --no-acl --no-owner -h ${HOST} -p ${PORT} -U ${USER_NAME} -d ${DB_NAME} ${DATA_FILE_PATH}
```
