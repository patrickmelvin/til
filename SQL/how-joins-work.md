`INNER JOIN` - Records exist in both Table_A and Table_B

| Table_A.id   | Table__B.table__a__id |
|--------------|-----------------------|
| 1            | 1                     |
| *NULL*       | NOT RETURNED          |
| NOT RETURNED | *NULL*                |

___

`LEFT OUTER JOIN` - Records exist in Table_A, but may not exist in TABLE_B

| Table_A.id   | Table__B.table__a__id |
|--------------|-----------------------|
| 1            | 1                     |
| *NULL*       | NOT RETURNED          |
| 2            | *NULL*                |

___

`RIGHT OUTER JOIN` - Records exist in Table_B, but may not exist in TABLE_A

| Table_A.id   | Table__B.table__a__id |
|--------------|-----------------------|
| 1            | 1                     |
| *NULL*       | 2                     |
| NOT RETURNED | *NULL*                |

___

`FULL OUTER JOIN` - Records exist in TABLE_A or TABLE_B, but may not match a record in the opposing table


| Table_A.id   | Table__B.table__a__id |
|--------------|-----------------------|
| 1            | 1                     |
| *NULL*       | 2                     |
| 2            | *NULL*                |
