#Docker Image Of MYSQL Database For Craft CMS
This is a Docker Image that pulls the latest mysql image, but makes some small changes to allow it to work with Craft CMS.

##Usage
There is only one required environmental variable to run this docker image. To see more options, check the (Official MySQL Docker Image)[https://hub.docker.com/_/mysql/].

    $ docker run --name mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw skilgarriff/craft-mysql

##Notes

### Group By

We had to change the MYSQL 'Group by' settings due to Craft version 2.5 not working correctly with these settings with an updated Mysql version. When Craft Version 3 is released, then we can revert back these changes as it is no longer needed to change the mysql group by default. This change to the Mysql configuration is stored in Craft.cnf.

Issue Documented: [Here](https://craftcms.stackexchange.com/questions/12084/getting-this-sql-error-group-by-incompatible-with-sql-mode-only-full-group-by/12473)

## License

The code is available under the [MIT License](/LICENSE).
