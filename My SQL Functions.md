## String Functions



### LENGTH

> 스트링의 길이를 바이트 단위로 반환한다.

**Syntax**

> LENGTH(*string*)
>
> | Parameter | Description                                  |
> | :-------- | :------------------------------------------- |
> | *string*  | Required. The string to count the length for |



---



### REPLACE

> `string`에서  from_string 을 `new_string` 으로 대체한다.

**Syntax**

> REPLACE(*string*, *from_string*, *new_string*)
>
> | Parameter     | Description                             |
> | :------------ | :-------------------------------------- |
> | *string*      | Required. The original string           |
> | *from_string* | Required. The substring to be replaced  |
> | *new_string*  | Required. The new replacement substring |

**Example**

> ```mysql
> select salary
> from employees;
> ```
>
> ```
> 2340
> 1198
> 9009
> 2341
> 9990
> ```
>
> ```mysql
> select replace(salary, '0', '')
> from employees;
> ```
>
> ```
> 234
> 1198
> 99
> 2341
> 999
> ```

## Numeric Functions



### AVG

> `expression` 의 평균 값을 반환합니다.

**Syntax**

> AVG(*expression*)
>
> | Parameter    | Description                                             |
> | :----------- | :------------------------------------------------------ |
> | *expression* | Required. A numeric value (can be a field or a formula) |



---



### CEIL

> `number` 보다 크거나 같은 정수 중 가장 작은 정수를 반환한다.

**Syntax**

> CEIL(*number*)
>
> 
>
> | Parameter | Description               |
> | :-------- | :------------------------ |
> | *number*  | Required. A numeric value |

**Example**

> ```mysql
> SELECT CEIL(25.6);
> ```
>
> ```
> 26
> ```