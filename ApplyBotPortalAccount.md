
整体流程：

  1. SNWG 在novoAccess申请对应的AAD账号和权限  --申请人
  2. 系统经理review ,并被审批.   --系统经理
  3. 发送邮件通知云团队创建AAD账号 -- 云团队
  4. 根据AAD账号配置到bot portal , 分配对应的角色和权限  --应用
      1. 配置botPortal 的用户和组
         adminsnwg@Novonordisk.partner.onmschina.cn
         链接如下： https://novonordisk.chinacloudsites.cn/portal
      2. 配置BotApplication AAD 授权用户ADD账号
         链接如下： https://portal.azure.cn/#view/Microsoft_AAD_IAM/ManagedAppMenuBlade/~/Users/objectId/9a43057c-0c06-42bd-a032-2aac3cb650a8/appId/78b1d414-8f36-42a2-acaf-5b0eaaa6494d/preferredSingleSignOnMode~/null/servicePrincipalType/Application/fromNav/


  5. 申请人验证机器人bot portal 的权限  --申请人
     验证bot portal是否可以通过ADD登录
        https://novonordisk.chinacloudsites.cn/portal
         
     验证Luis的Portal 是否可以ADD登录
     https://luis.azure.cn/application
