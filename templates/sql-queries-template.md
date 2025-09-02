# SQL Lab — Filters & Security Context

## Sample Queries
```sql
-- Filter failed logins in last 24h
SELECT user, ip, ts 
FROM auth_logs
WHERE success = 0 AND ts >= NOW() - INTERVAL '24 hours';

-- Aggregate by IP
SELECT ip, COUNT(*) AS failures
FROM auth_logs
WHERE success = 0
GROUP BY ip
ORDER BY failures DESC
LIMIT 20;
```

## Notes
- How query aids incident detection or audit.
- Potential false positives / data quality caveats.
