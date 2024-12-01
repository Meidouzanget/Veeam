# Veeam
Veeam

### Veeam Backup & Replication 12 安装和激活

#### 下载
直接到官网注册，下载 Veeam Backup & Replication 12社区版

未激活之前属于社区版，拥有十个备份授权；激活之后自动转变为企业版

https://www.veeam.com/cn/products/downloads.html?ad=top-sub-menu

#### 下载替换文件
[替换文件下载](https://link.zhihu.com/?target=https%3A//songxwn.com/file/Veeam_12_P.7z)

下载后解压，会有下列文件

```
VeeamLicense.dll
#替换文件
Veeam_ASv11_1500.lic
Veeam_BackupRep_v12_5000_1.lic
#授权文件
```

#### 停止服务和替换文件
安装完软件之后

使用管理员运行PowerShell 执行下面命令：

```
get-service -displayname Veeam* | stop-service
get-service -displayname Veeam*
```

然后进入C:\Program Files\Common Files\Veeam 目录下，将VeeamLicense.dll 覆盖到其目录下。

#### 启动服务
然后运行所有服务
```
get-service -displayname Veeam* | start-service
```

#### 导入
打开Veeam Backup & Replication Console 软件，点击左上角的菜单，选择License选项，点击install，选择

Veeam_BackupRep_v12_5000_1.lic 文件导入安装即可激活。
