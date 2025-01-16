
# 2025

## Todolist 


#### token失效的处理
场景：
当token失效的时候，界面的上线和下线都无法操作，请帮忙核对一下对于
Server给出的token失效是否有处理逻辑和应对，多谢。
优先级：低
提出人： TALU




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

### （微信端）  SD的同事，SD发送结束转人工，用户在左侧无法取消，无法退出转人工 （偶尔出现）  微信端
如果找不到原因，是不是可以先放开这里，提示一下用户就可以，不用强制用户，不能操作

 

### （ 微信端） 我发现 就是比如我在和客户1聊天 然后在回复客户1 这时候如果客户2进线说话了 我打给客户1的消息就会自动发给客户2 （SD表示多次）
这个问题，需要内部测试验证一下,有可能使我们之前的场景没有覆盖到；如果有问题或者疑问，我这边可以联系SD的一起看下。  微信端

 

 ### （Teams端）ZJQH (Huang Jing)使用teams报单时，SDWQZY回复的内容，ZJQH (Huang Jing)接收不到    Teams端
 

 ###  （微信端） SDWQZY在11月05日15:29分给用户（XUYX）发送的消息，XUYX未收到，具体发送的内容如下
"您的签到表AMN-XUYX-241021-002182738目前已经更新，张晓宁老师已经不标黄，请您务必通过智会系统点击同步iwe数据按钮同步确认（可以立刻操作）。请务必确保iwe结果合格在操作关会。另外如若会议被跟会，请务必等待返还结果为合格后在进行关会。如若已经被判定第三方跟会不合格，请将合格的签到表发送到shensu@novonordisk.com的邮箱中，请第三方团队帮您重新判定结果。"

附件是用户那边聊天记录以及SD这边的聊天记录对比图，辛苦帮忙查明是因为字数问题还是因为对话中包含了某些特殊字符，谢谢


