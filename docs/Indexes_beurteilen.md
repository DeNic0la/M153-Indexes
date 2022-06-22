# Wie kann ein Index beurteilt werden?

[Zurück](../README.md)
<br/><br/>

### Der Hauptgrund für die Verwendung eines Indexes ist die Effizienz. Daher muss die Dauer für die Ausführung einer Abfrage gemessen werden können. Erstellen Sie mind. ein Beispiel, wie die Dauer einer Abfrage gemessen und für die weitere Verarbeitung gespeichert werden kann.
Die Performance Verbesserung eines Index kann beurteilt werden, indem man eine Abfrage auf gewisse Daten ohne Index
durchführt und eine Abfrage auf dieselben Daten mithilfe eines Index wiederholt.
## Beispiel:
Abfrage mit Index:
```sql
SET @t1 = GETDATE();
SELECT * FROM Tabelle WITH(INDEX(name_des_indexes));
SET @t2 = GETDATE();
DECLARE @TimeFirstQuery INT = DATEDIFF(MILLISECOND,@t1,@t2);
```
Abfrage ohne Index: 
```sql
SET @t1 = GETDATE();
SELECT * FROM Tabelle;
SET @t2 = GETDATE();
DECLARE @TimeSecondQuery INT = DATEDIFF(millisecond,@t1,@t2);
```



