#### Give a star before you see it. Ha ha ha ~ ~

Generates a protobuf file from your PostgreSQL database.

### Uses

##### Tips:  If your operating system is windows, the default encoding of windows command line is "GBK", you need to change it to "UTF-8", otherwise the generated file will be messed up. 

```
$ sql2pb -h

Usage of sql2pb:
  -db string
        the database type (default "postgres")
  -field_style string
        gen protobuf field style, sql_pb | sqlPb (default "sqlPb")
  -go_package string
        the protocol buffer go_package. defaults to the database schema.
  -host string
        the database host (default "localhost")
  -ignore_columns string
        a comma spaced list of PostgreSQL columns to ignore
  -ignore_tables string
        a comma spaced list of tables to ignore
  -package string
        the protocol buffer package. defaults to the database schema.
  -password string
        the database password
  -port int
        the database port (default 5432)
  -schema string
        the database schema
  -service_name string
        the protobuf service name , defaults to the database schema.
  -table string
        the table schema，multiple tables ',' split.  (default "*")
  -user string
        the database user (default "postgres")

```

```
$ sql2pb -go_package ./pb -host localhost -package pb -password yourpwd -port 5432 -schema public -service_name usersrv -user postgres > usersrv.proto
```

#### Thanks for schemabuf
    schemabuf : https://github.com/mcos/schemabuf
