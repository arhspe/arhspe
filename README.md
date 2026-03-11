```sql
WITH developer AS (
    SELECT
        'Arthur Pereira' AS name,
        'arhspe' AS username,
        'São Paulo, Brazil' AS location,
        'ADS at Centro Paula Souza' AS education
),
stack AS (
    SELECT UNNEST(ARRAY['C', 'py', 'postgres']) AS technology
),
interests AS (
    SELECT UNNEST(ARRAY['databases', 'backend', 'data']) AS interest
)
SELECT *
FROM developer
JOIN stack ON TRUE
JOIN interests ON TRUE;
```
