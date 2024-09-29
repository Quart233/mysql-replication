# Mysql replica

## Crete replica user
```sql
# replica user
CREATE USER 'repuser'@'%' IDENTIFIED BY 'ChangeMe';

# permission
GRANT REPLICATION SLAVE,REPLICATION CLIENT ON *.* TO 'repuser'@'%';

FLUSH PRIVILEGES;
```

## Test
Prune volume each time