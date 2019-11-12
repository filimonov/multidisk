```sql
SELECT
    name,
    path,
    formatReadableSize(free_space) AS free,
    formatReadableSize(total_space) AS total,
    formatReadableSize(keep_free_space) AS reserved
FROM system.disks
```

```
┌─name────┬─path─────────────────┬─free─────┬─total────┬─reserved─┐
│ default │ /var/lib/clickhouse/ │ 7.49 GiB │ 9.63 GiB │ 0.00 B   │
└─────────┴──────────────────────┴──────────┴──────────┴──────────┘

1 rows in set. Elapsed: 0.001 sec. 
```
