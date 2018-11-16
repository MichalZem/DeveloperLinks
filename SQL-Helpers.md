# SQL Helpers Query

## Close all connections to a database
```sql
USE [master];

DECLARE @kill varchar(8000) = '';  
SELECT @kill = @kill + 'kill ' + CONVERT(varchar(5), session_id) + ';'  
FROM sys.dm_exec_sessions
WHERE database_id  = db_id('MyDB')

EXEC(@kill);
```

## Find waiting Queries which are block by other running Queries (Wait) 
```sql
SELECT
	dowt.session_id
	,dowt.wait_duration_ms
	,dowt.wait_type
	,dowt.blocking_session_id
	,dese.host_name as HostName
	,der.command
	,der.percent_complete
	,der.cpu_time
	,der.total_elapsed_time
	,der.reads
	,der.writes
	,der.logical_reads
	,der.row_count
	,dest.text AS QueryText
	,dest.dbid AS DatabaseID
	,deqp.query_plan
	,der.plan_handle
FROM sys.dm_os_waiting_tasks as dowt
INNER JOIN sys.dm_exec_sessions as dese
	ON dowt.session_id = dese.session_id
INNER JOIN sys.dm_exec_requests as der
	ON dese.session_id = der.session_id
CROSS APPLY sys.dm_exec_sql_text(der.plan_handle) as dest
CROSS APPLY sys.dm_exec_query_plan(der.plan_handle) as deqp
WHERE dowt.session_id > 50
```
