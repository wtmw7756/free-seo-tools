# RackNerd VPS主机Root密码修改指南（控制面板与SSH两种方法）

RackNerd 作为高性价比的美国VPS服务商，其低价年付方案深受外贸用户和预算有限的开发者青睐。虽然线路未采用CN2优化，但稳定的国际带宽完全能满足基础业务需求。本文将详细介绍两种修改Root密码的实用方法。

## 一、通过SSH命令行修改密码（需已登录服务器）

1. 使用SSH客户端连接至您的RackNerd VPS
2. 在终端输入命令：`passwd`
3. 根据提示连续两次输入新密码（输入时不会显示字符）
4. 出现`password updated successfully`即表示修改成功

## 二、通过控制面板修改密码（推荐新手使用）

### 步骤1：获取面板登录凭证
- 检查注册邮箱中的初始开通邮件（主题通常包含"Welcome"或"Server Details"）
- 若邮件遗失，可登录RackNerd账户后台查看站内信：
  1. 访问[客户中心](https://bit.ly/Rack_Nerd)
  2. 导航至`Services → My Services`
  3. 点击`Email History`查看历史邮件

👉 [【点击查看】2025年最新 Racknerd 优惠码及特价云服务器方案汇总](https://bit.ly/Rack_Nerd)

### 步骤2：登录SolusVM控制面板
1. 在服务器管理页面找到`Control Panel`按钮
2. 使用邮件中的用户名/密码登录
3. 若忘记密码，可通过`Forgot Password`功能重置

### 步骤3：修改Root密码
1. 进入面板后选择`Root Password Modification`
2. 输入并确认新密码（建议包含大小写字母+数字）
3. 点击`Change Password`完成设置

## 重要提示
- 修改密码后需重启SSH服务生效（或等待5分钟自动同步）
- 建议定期更换密码以提升安全性
- 同一账户下的多台VPS需要分别修改密码

通过控制面板修改的优势在于可视化操作，且能避免因SSH连接异常导致的密码修改失败。如需更详细的服务器管理教程，可参考RackNerd官方知识库文档。