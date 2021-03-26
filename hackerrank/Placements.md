# [Placements](https://www.hackerrank.com/challenges/placements/problem?h_r=next-challenge&h_v=zen)



## 문제

> You are given three tables: *Students*, *Friends* and *Packages.* *Students* contains two columns: *ID* and *Name*. *Friends* contains two columns: *ID* and *Friend_ID* (*ID* of the ONLY best friend). *Packages* contains two columns: *ID* and *Salary* (offered salary in $ thousands per month).
>
> ![img](https://s3.amazonaws.com/hr-challenge-images/12895/1443820186-2a9b4939a8-1.png)
>
> Write a query to output the names of those students whose best friends got offered a higher salary than them. Names must be ordered by the salary amount offered to the best friends. It is guaranteed that no two students got same salary offer.
>
> **Sample Input**
>
> ![img](https://s3.amazonaws.com/hr-challenge-images/12895/1443820079-9bd1e231b1-2_1.png) ![img](https://s3.amazonaws.com/hr-challenge-images/12895/1443820100-adb691b2f5-2_2.png)
>
> **Sample Output**
>
> ```
> Samantha
> Julia
> Scarlet
> ```
>
> 
> **Explanation**
>
> See the following table:
>
> ![img](https://s3.amazonaws.com/hr-challenge-images/12895/1443819966-c37c146d27-3.png)
>
> Now,
>
> - *Samantha's* best friend got offered a higher salary than her at 11.55
> - *Julia's* best friend got offered a higher salary than her at 12.12
> - *Scarlet's* best friend got offered a higher salary than her at 15.2
> - *Ashley's* best friend did NOT get offered a higher salary than her
>
> The name output, when ordered by the salary offered to their friends, will be:
>
> - *Samantha*
> - *Julia*
> - *Scarlet*



## 나의 풀이

```sql
select s.name
from students s
join packages p on s.id = p.id
join friends f on s.id = f.id
join packages fp on f.friend_id = fp.id
where p.salary < fp.salary
order by fp.salary;
```

