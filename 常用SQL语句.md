#常用SQL语句
##复杂联查
1. 联查评论

``` sql
select C1.id from_id,C1.nickname from_name,C2.id to_id,C2.nickname to_name,SC2.content to_content,SC.* 
from social_comment SC 
left join customer C1 on C1.id = SC.customer_id 
left join social_comment SC2 on SC2.id = SC.to_social_id 
left join customer C2 on C2.id = SC2.customer_id 
where SC.social_id = 1
```

##时间处理
1. 查询60天内的数据

``` sql
where TO_DAYS(S.create_time) > TO_DAYS(now()) - 60
```