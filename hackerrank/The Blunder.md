# [The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem)



## 문제

> Samantha was tasked with calculating the average monthly salaries for all employees in the **EMPLOYEES** table, but did not realize her keyboard's key was broken until after completing the calculation. She wants your help finding the difference between her miscalculation (using salaries with any zeroes removed), and the actual average salary.
>
> Write a query calculating the amount of error (i.e.: average monthly salaries), and round it up to the next integer.
>
> **Input Format**
>
> The **EMPLOYEES** table is described as follows:
>
> ![img](https://s3.amazonaws.com/hr-challenge-images/12893/1443817108-adc2235c81-1.png)
>
> **Note:** *Salary* is measured in dollars per month and its value is .
>
> **Sample Input**
>
> ![img](https://s3.amazonaws.com/hr-challenge-images/12893/1443817161-299cc6eb7f-2.png)
>
> **Sample Output**
>
> ```
> 2061
> ```
>
> **Explanation**
>
> The table below shows the salaries *without zeroes* as they were entered by Samantha:
>
> ![img](https://s3.amazonaws.com/hr-challenge-images/12893/1443817229-eb00d44a3b-3.png)
>
> Samantha computes an average salary of . The *actual* average salary is .
>
> The resulting error between the two calculations is which, when rounded to the next integer, is .



### MySQL 풀이 

```mysql
select ceil(avg(salary) - avg(replace(salary, '0', '')))
from employees;
```



