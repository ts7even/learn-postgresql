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
createuser --interactive
      
      name of role to add: rainman
 
 createdb learnPost
 
*  psql -d myDatabaseName #  Use the -d option to connect to the database you created (without specifying a database, psql will try to access a database that matches your username).

To go to your database when in sudo directory (not postgres)
* sudo -iu postgres
* psql -d myDatabaseName
