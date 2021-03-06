ss-panel
========

A simple front end of [Shadowsocks manyuser](https://github.com/mengskysama/shadowsocks/tree/manyuser
)  

[Demo](https://cattt.com) [中文安装文档](https://github.com/orvice/ss-panel/wiki/Install-Guide-zh_cn)

### Upgrade from 0.X

[Read this](https://github.com/orvice/ss-panel/blob/master/upgrade_to_v2.md)

### Requirements
* PHP >= 5.4
* PDO Extension

### Install
* Import sql/*.sql to your MySQL Database
* Rename lib/config-sample.php to config.php,and edit the database infomation.
* Enjoy it.

### Admin
* The user who uid is 1 is Admin by default.
* You can Add User ID into table 'ss_user_admin'

### Send mail using mail-gun
Run:

```
$ curl -sS https://getcomposer.org/installer | php
$ php composer.phar  install
```
更新内容：
添加弹窗显示二维码和配置信息

![qq 20150516102428](https://cloud.githubusercontent.com/assets/11162054/7664380/12f6a418-fbb7-11e4-90aa-d95b7c53ca86.png)

![qq 20150516102541](https://cloud.githubusercontent.com/assets/11162054/7664419/b2e55cd4-fbb8-11e4-8131-cb86d30c4ed4.png)

新添管理员中心的（网页）用户表优化 ,更新DataTables 至 1.10.7 并汉化部分中文提示

![qq 20150511101621](https://cloud.githubusercontent.com/assets/11162054/7557585/e0e0b55c-f7c6-11e4-8569-695fd7cd4785.png)

![qq 20150511102255](https://cloud.githubusercontent.com/assets/11162054/7557633/d1a2c142-f7c7-11e4-9047-99ca7fd3c3f7.png)

![qq 20150511102328](https://cloud.githubusercontent.com/assets/11162054/7557634/d5c022a6-f7c7-11e4-843c-3783ed02c3ef.png)

以上图中数据为测试的

新增smtp邮件

修改：

移动以下内容至新文件Public_javascript.php并在所有调用<?php require_once '_footer.php'; ?>的文件加入<?php include_once '../Public_javascript.php'; ?>调用。
```
<!-- jQuery 2.1.3 -->
<script src="../asset/js/jQuery.min.js"></script>
<!-- Bootstrap 3.3.2 JS -->
<script src="../asset/js/bootstrap.min.js" type="text/javascript"></script>
<!-- SlimScroll -->
<script src="../asset/plugins/slimScroll/jquery.slimscroll.min.js" type="text/javascript"></script>
<!-- FastClick -->
<script src='../asset/plugins/fastclick/fastclick.min.js'></script>
<!-- AdminLTE App -->
<script src="../asset/js/app.min.js" type="text/javascript"></script>
```
### Thanks to

* [AdminLTE](https://github.com/almasaeed2010/AdminLTE)
* [Medoo](https://github.com/catfan/Medoo)

