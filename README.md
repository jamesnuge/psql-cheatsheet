# Nuge's PSQL Cheatsheet

## Data Exporting

To export a database to a data file use the following command

```
    pg_backup ${DB_NAME} > ${OUTPUT_FILE}
```

## Data Importing

To import a data file from an export use the following command

```
    pg_restore --verbose --clean --no-acl --no-owner -h ${HOST} -p ${PORT} -U ${USER_NAME} -d ${DB_NAME} ${DATA_FILE_PATH}
```
