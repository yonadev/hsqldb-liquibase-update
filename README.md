g`"ase layer for Liquibase update
==================================

This image is created as base layer. To use it, derive an image from it and add the root change log file to as /changelogs/changelog with your preferred file extension.

This image runs [Liquibase update](http://www.liquibase.org/documentation/update.html) with the change log /changelogs/changelog.\* and the HSQLDB JDBC driver.

#### Example use

```
docker run -i \
  -e USER=sa \
  -e PASSWORD=TopSecret \
  -e URL=url \
  your/image
```

The environment variables required are:

USER - the user to the target database  
PASSWORD - password to the target database  
URL - the JDBC URL

The implementation is based on [the work of Tom Beresford](https://hub.docker.com/r/beresfordt/pg-liquibase-update/~/dockerfile/).
