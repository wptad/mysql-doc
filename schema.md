## show tables
```
SELECT *
FROM INFORMATION_SCHEMA.TABLES
WHERE table_schema = '';
			
```

## show columns
```
select *
from `information_schema`.`COLUMNS` 
where `table_schema` = '';

```



## print tables and columns
```
select  `TABLES`.`TABLE_NAME`,`TABLES`.`TABLE_COMMENT`, `COLUMNS`.`COLUMN_NAME`, `COLUMNS`.`DATA_TYPE`,  `COLUMNS`.`COLUMN_KEY`,`COLUMNS`.`COLUMN_COMMENT`
from information_schema.`TABLES` inner join information_schema.`COLUMNS` on `TABLES`.TABLE_NAME = `COLUMNS`.`TABLE_NAME`
where `TABLES`.`table_schema` = ''
order by `TABLES`.`TABLE_NAME`,  `COLUMNS`.`ORDINAL_POSITION` ,`COLUMNS`.`COLUMN_NAME`
```
