**制作U盘启动盘**

1. 首先准备一个格式化后的空白U盘（8G及以上）
   1. 在Microsoft官网下载一个Windows 10安装程序

->执行它

->选择要安装的系统：

语言：中文（简体）

版本：Windows10

体系结构：64位（x64）

->选择要使用的介质：U盘

->向选择的U盘中下载Windows 10

这时一个U盘启动盘就做好了



**进BIOS**

台式机一般是Del，不同电脑进入键不同，自行百度

开机，按键进入主板的BIOS设置界面

找到关于“启动”的选项，其中会有一个启动的顺序（比如Boot Option #1、Boot Option #2 ...），在首选的启动设备处选择“UEFI：你的U盘名字”，这样就会第一个去找这个设备来引导系统，最后按一下F10，进行设置的保存，并且退出BIOS



**安装系统**

按照Windows的提示安装系统即可，这里别的步骤都不太重要，重要的是进行分区



**分区**

一个驱动器对应自己装进去的一块固态、机械硬盘，一个驱动器可能会分成多个分区，这时我们需要将几个分区的大小加和猜测出哪个驱动器是哪个硬盘。为了将某快硬盘上的所有分区合并成一个，右键删除这些分区，最终将合并成“驱动器X未分配的空间”。为什么硬盘容量总是小于宣称的容量？因为硬盘厂商使用1000进制，而非1024进制



**修改引导**

当分区也做完后，比较智能的电脑会自动将下次启动设置为从硬盘引导

但是也有不太智能的，下次还会从U盘引导，这就需要我们重启后再次进入BIOS，然后将启动设置为从硬盘引导（因为此时系统已经安装在硬盘中了）