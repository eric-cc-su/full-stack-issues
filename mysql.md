## **MySQL**

### Can't connect to local MySQL server

Make sure that you've started your MySQL server. There are command line options or GUIs that you can use for this.

### Access Denied

Slowly re-type your password or make sure that you're using the right username and host. Sometimes you will need to
explicitly tell MySQL to log you in with a username and password using the -u and -p options.

[Connecting to the MySQL Server](https://dev.mysql.com/doc/refman/5.7/en/connecting.html):

- logging in with a username: `mysql -u bob`
- logging in with a username and password: `mysql -u bob -p`
- logging in with a username and password and your password is "thebuilder": `mysql -u bob -pthebuilder` OR `mysql -u bob --password=thebuilder`
- logging in with a username and password to the table "bricks": `mysql -u bob -p bricks`

**But I swear my credentials are right!** - If you're using a virtual machine, make sure you're SSH'd into your machine
before you try logging in to MySQL. (Yes, I've done this before)

EDIT: You should also make sure that any users you set up in MySQL have proper permissions to access or edit the
database you need.

### "Field Doesn't Have a Default Value"

This sometimes occurs if you're applying new changes and for some reason your database doesn't get
 the memo that a column was given a default value. This can be fixed with an 
 [ALTER TABLE](http://dev.mysql.com/doc/refman/5.7/en/alter-table.html) command.

ex. `ALTER TABLE table_name ALTER column_name SET DEFAULT NULL;` would set the default as NULL
