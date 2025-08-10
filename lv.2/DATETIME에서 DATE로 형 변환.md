문제: https://school.programmers.co.kr/learn/courses/30/lessons/59414?language=mysql

---

Oracle

```SQL
SELECT 
    ANIMAL_ID,
    NAME,
    TO_CHAR(DATETIME, 'YYYY-MM-DD') AS 날짜
FROM ANIMAL_INS
ORDER BY ANIMAL_ID
```

---

MySQL

```SQL
SELECT 
    ANIMAL_ID,
    NAME,
    DATE_FORMAT(DATETIME, '%Y-%m-%d') AS '날짜'
FROM ANIMAL_INS
ORDER BY ANIMAL_ID
```

---
