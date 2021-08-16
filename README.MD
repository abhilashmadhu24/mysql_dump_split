Hi,

Sharing this bash script to extract only required table from a mysqldump.sql file. I hope this will help in scenarios like DBA's need to restore a specific
table from a huge dump file .

Courtesy : https://kedar.nitty-witty.com/blog/mydumpsplitter-extract-tables-from-mysql-dump-shell-script

```
git clone https://github.com/abhilashmadhu24/mysql_dump_split.git
cd mysql_dump_split
chmod +x mysql_dump_split
sh DumpSplitter.sh <dump_file> #Extracts all tables from provided dump file
sh DumpSplitter.sh <dump_file> <table_name> #Extracts mentioned table name only
sh DumpSplitter.sh <dump_file> <Expression> #Extract tables from dump for specified regular expression

```

```
abhilashmadhu@-Latitude-3410:~/mysql_script$ sh DumpSplitter.sh mysqldb-16-Aug-2021-03-00-01.sql tbl_phone
Extracting tbl_phone...
1 Table extracted from mysqldb-16-Aug-2021-03-00-01.sql at /home/abhilashmadhu/mysql_script/tbl_phone.sql
```
