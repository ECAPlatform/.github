# 2024
## Todolist
### CR
1. 记录用户最后登录时间，如果超期没有登录，体现出来


### 优化点&bug
#### 如何触发转人工
目前转人工是通过 用户的输入文字是否包含“转人工”触发的，是否修正为完全等于“转人工”三个字（待讨论），出现问题场景： 如果用户转人工之后，再次输入，“”我想知道转人工的工作时间“”
由于包含“转人工”，目前认定为转人工命令，仅仅提示了用户，没有把”我想知道转人工的工作时间“发送给SD
#### 特殊字符处理
特殊字符的处理（不是升级导致的，放在后续集中修复）

### 优化派单逻辑
优化SD坐席的分配逻辑，根据华老师的建议，汇总如下：假如SD 3个人，A，B，C， 每个坐席最多接待3个用户，当每个坐席接待量不满的情况下，A，B，C一直安装顺序轮流安排；坐席接待量满的情况下，剩下的接待量不满SD安装顺序轮流安排。

### 转人工的导出聊天日志

导出转人工的日志的时候，没有反应，目前聊天日志数据量比较大，需要进行性能优化

报错原因：
Caused by: java.sql.SQLSyntaxErrorException: Expression #4 of SELECT list is not in GROUP BY clause and contains nonaggregated column 'm2.art_text' which is not functionally dependent on columns in GROUP BY clause; this is incompatible with sql_mode=only_full_group_by


