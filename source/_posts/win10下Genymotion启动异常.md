---
title: win10下Genymotion启动异常
date: 2019-01-24 10:10:39
tags: [模拟器, win10, 安卓, 虚拟机]
---

### 这边是做下问题的记录方便以后重复出现

之前pc 系统换了ssd升级到了固态后，发现Genymotion模拟器不能用了，启动报错是cpu不支持虚拟化。

然后就fn+f2进了Bios模式看了，虚拟化是开启的。为什么这样尼。

下面记录下问题，是因为Hyper-V服务默认开启了。

手动关闭就好了。

右键管理员权限启动win10下的powershell 工具。

```linux
bcdedit /set hypervisorlaunchtype off 
```

重新启动模拟器就ok了。