# proj36-dim-sum
### 项目名称
dim-sum自研操作系统

### 项目描述

dim-sum操作系统是由谢宝友开发的自研操作系统，支持运行于qemu arm64中。

其目标是替代开源Linux操作系统，并能用于生产环境的服务器系统中。期望10年内实现这个目标。

具体目标是：

1. 在Linux操作系统被国内限制使用的情况下，有可替代的操作系统可用。

2. 真正自研，而不是在现有的Linux操作系统基础上进行拉皮。

3. 为国内培养操作系统研发型人才。

当前项目实现源码位于：https://gitee.com/xiebaoyou/dim-sum

### 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道



### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求



### 项目导师

谢宝友

* github
* gitee https://gitee.com/xiebaoyou/
* email scxby@163.com



### 难度

中等



### 特征

- 完全自研
- 支持arm 64 / x86_64多核系统
- 兼容Linux
- 平滑支持Android / Centos / ubuntu



### 文档

- https://gitee.com/xiebaoyou/documents

### License

[GPL-3.0-only](https://opensource.org/licenses/GPL-3.0)



## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

### 第一题：支持x86_64

- 在qemu中启动x86-64,     正常运行dim-sum操作系统

### 第二题：添加网络协议栈支持

- dim-sum目前移植了lwip以支持网络协议栈，希望能参照linux 1.1.3实现一个简单的网络协议栈
- 实现更强大的网络协议栈是更受欢迎的
- 重点实现 tcp/udp 的 v4/v6版本
- 需要注意同步与互斥，特别是多核系统中的同步与互斥，并且避免性能瓶颈
- 需要特别注意网络攻击防范

### 第三题：支持busybox

- 目前，dim-sum还不支持运行用户态应用程序，需要借鉴linux支持常见的 elf/flat/sh 等类型的用户态应用程序
- 需要深刻的理解不同应用程序的二进制格式
- 需要深刻的理解应用程序的内存维护、进程生命周期管理、系统调用。