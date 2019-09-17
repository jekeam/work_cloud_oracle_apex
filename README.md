# Simple word cloud for Oracle APEX (Beta)

For correct operation, the JQ library is required, 3.1.1 or under, for example: [3.1.1](https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js).

SQL Example:

```
select 
  dbms_random.string('u', 1)||dbms_random.string('l', 5) as name,
  round(dbms_random.value(20, 45)) as cnt,
  to_char(trunc(dbms_random.value(0, 256*256*256)), 'fm0xxxxx') as color
from dual
connect by level < round(dbms_random.value(30,50))
```

![img](/screenshot.png)
