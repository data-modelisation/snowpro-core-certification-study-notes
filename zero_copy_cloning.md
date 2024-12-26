# Zero-copy cloning 

Take snapshot + meta data operation.
Cloned object independent from original table 
Creating backup for dev purposes 
Typically combined with time travel 

```sql 
CREATE TABLE table_new
CLONE table_source
```

Cloning from specific point in time is possible :

```
CREATE TABLE table_new
CLONE table_source
BEFORE (TIMESTAMP => 'tumestamp')
```

## Cloning objects 
Cloning objects : 
- Database 
- Schema 
- Table 
- Stream 
- File Format 
- Sequence 
- Task 
 
- Stage - Named internal stages <ins>not</ins> cloned
- Pipe - only for external stages 


Cloning a database or schema will clone <ins>all contained objects </ins>.  
Privileges will always be inherited to child objects <ins> never to source object itself</ins>.   
Load history meta data is not copied. *Loaded data can be loaded again.*   

## What privileges are needed ?

Table => **Select**   
Pipe, Stream, Task => **Owner**   
All other objects => **Usage**   
