문제 출처: https://school.programmers.co.kr/learn/courses/30/lessons/59405?language=oracle

참고 블로그: https://ha-genie.tistory.com/9

---

MySQL, LIMIT 이용

```SQL
SELECT NAME
FROM ANIMAL_INS
ORDER BY DATETIME
LIMIT 1;
```

---

ORACLE, 인라인 뷰 이용 

```SQL
SELECT NAME
FROM 
(
    SELECT * 
    FROM ANIMAL_INS
    ORDER BY DATETIME
)
WHERE ROWNUM = 1
```

---

실행 순서

FROM - WHERE - GROUP BY - HAVING - SELECT - ORDER BY
