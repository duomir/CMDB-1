# CMDB
基于Django的可扩展CMDB平台

## 架构
CMDB由三部分组成，分别是
* 资产采集
* API接口
* 后台管理

**资产采集**
通过paramiko创建SSH链接，并执行远程操作获取服务器资产信息。同时负责数据的筛选（结构化），并通过API接口发送到服务端。
本项目的资产采集部分代码在`Controller`目录中。

**API接口**
三个主要功能，首先是接受采集的资产信息，并入库，然后是资产变更的记录和处理，最后是给自动化运维中的第三方程序提供接口。
本项目中的API接口和后台管理整合到了一起。

**后台管理**
为运维人员提供交互：资产管理、报表生成、统计等等。
本项目中的API接口和后台管理整合到了一起。