# learn-postgresql

## Set up for linux
default user when you install is postgres, and to access the postgres user is 
* sudo -iu postgres
* initdb --local=en_US.UTF-8 -E UTF8 -D /var/lib/postgres/data # 

https://wiki.archlinux.org/title/PostgreSQL

Success. You can now start the database server using:

    pg_ctl -D /var/lib/postgres/data -l logfile start
    
systemctl enable  postgresql.service    
systemctl start  postgresql.service 


## Create User and Database and Connect to database
createuser --interactive -P

      
      name of role to add: rainman
 
 createdb learnPost
 
*  psql -d myDatabaseName #  Use the -d option to connect to the database you created (without specifying a database, psql will try to access a database that matches your username).

To go to your database when in sudo directory (not postgres)
* sudo -iu postgres
* psql -d learnPost
* \c connects to database
* pgadmin4

Add your PostgreSQL server to pgAdmin
Now add the PostgreSQL Server in the pgAdmin Control Panel by clicking on "Add New Server".

Give your server configuration a name.

Under the "Connection" Tab set the following properties

Use 127.0.0.1 (localhost) as Hostname
The port, your server is listening on. (By default this is 5432)
Use postgres as Maintenance database
The username and password of the PostgeSQL user you created so far
If this is a lucky day everything should work now!
