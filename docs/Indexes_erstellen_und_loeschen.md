# Wie wird ein Index erstellt, gelöscht usw.?
[Zurück](../README.md)
<br/><br/>
### Syntax und Beispiele wie ein normaler Index erstellt, gelöscht und verwendet wird.

## Index erstellen
Normaler index auf einer Tabelle. Duplikate sind erlaubt.
```sql
CREATE INDEX name_des_indexes
ON table_name (col1, col2, col_n, ...);
```
Unique Index, keine Duplikate möglich.
```sql
CREATE UNIQUE INDEX name_des_indexes
ON table_name (col1, col2, col_n, ...);
```
