```sql
CREATE TABLE profile (
    id SERIAL PRIMARY KEY,
    name TEXT NOT NULL,
    username TEXT NOT NULL,
    education TEXT NOT NULL,
    focus TEXT NOT NULL
);

CREATE TABLE stack (
    id SERIAL PRIMARY KEY,
    profile_id INTEGER REFERENCES profile(id),
    technology TEXT NOT NULL
);

INSERT INTO profile (name, username, education, focus)
VALUES (
    'arthur pereira',
    'arhspe',
    'technical degree in systems development',
    'solving real-world problems through code, data, and well-structured systems'
);

INSERT INTO stack (profile_id, technology)
VALUES
    (1, 'python'),
    (1, 'postgres'),
    (1, 'mysql');

SELECT
    p.name,
    p.username,
    p.education,
    STRING_AGG(s.technology, ', ') AS stack,
    p.focus
FROM profile p
JOIN stack s ON s.profile_id = p.id
GROUP BY p.name, p.username, p.education, p.focus;

```
