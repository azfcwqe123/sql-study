문제: https://school.programmers.co.kr/learn/courses/30/lessons/273710

---

MySQL

```SQL
SELECT
    A.ITEM_ID, # ITEM_ID만 쓰면 에러 발생
    ITEM_NAME
FROM
    ITEM_INFO A
INNER JOIN
    ITEM_TREE B
    ON A.ITEM_ID = B.ITEM_ID
WHERE
    B.PARENT_ITEM_ID IS NULL
ORDER BY
    ITEM_ID
```

---

실패 (1052, "Column 'ITEM_ID' in field list is ambiguous")

- ITEM_ID라는 컬럼이 어떤 테이블에 있는 건지 MySQL이 구분 못한다는 뜻. 
- 보통 JOIN을 했을 때, 양쪽 테이블에 같은 컬럼명이 있을 경우 발생

