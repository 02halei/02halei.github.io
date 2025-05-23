# 前言
 **出一期deepseek的本地部署教程**
> 软件使用：ollama
> 系统：Windows
---
# 硬件
* 首先你需要一个硬件部署，这里我用的机架式服务器。
## 二手机架式服务器
**此方案正在优化中！！仅作参考**
> 很火的deepseek，时常难受的未响应~~想玩模型没硬件...就这样我的机架式服务器旅程开始了。
## 硬件信息
* CPU：[Intel 至强 Platinum 8259CL](https://www.xincanshu.com/cpu/Intel_Xeon_Platinum_8259CL/)
**淘宝240×2=480¥**
* 浪潮 (Inspur)SA5212M5双路2U服务器
**淘宝950¥**
* DDR4 ECC 服务器内存2666MHz（两颗CPU共能上12根）
> 因为CPU功耗为210W，主板供电205W，所以需要如视频解锁功耗墙！
## [可参照视频](https://www.bilibili.com/video/BV1YEPvepEvf/?spm_id_from=333.337.search-card.all.click)

`Gmeek-html<iframe src="//player.bilibili.com/player.html?isOutside=true&aid=114063795427174&bvid=BV1YEPvepEvf&cid=28569963696&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>`

## 视频刷机包
浪潮解锁大功率刷机板驱动以及刷机程序包：
百度网盘
https://pan.baidu.com/s/1ZTUDP7e7YJT8pFWjq2HPow?pwd=dkqc
提取码: dkqc
## 视频中给出的价格和配置信息
* 浪潮准系统SA5212M5 带双电+50元升级40Gx722网卡 940元
* 至强可拓展2代8259CL 240*2 480元
* 三星RECC DDR4 2666Mhz 16G 现价格83元每根x12 996元
* 刷机板以及线材 40元
* 浪潮3008直通卡 80元
# ollama部署
* 下载[ollama](https://ollama.com/)并运行安装程序。
* win+R打开cmd，输入命令下载模型。
> 注意ollama默认下载在C盘，模型同样，请确保C盘空间足够！[如需更改磁盘请参考文章](https://02halei.github.io/post/%E3%80%90AI%E2%80%94%E2%80%94OLLAMA%E3%80%91Ollama-bu-shu-ben-di-mo-xing-%EF%BC%81%EF%BC%88-bian-xie-zhong-%EF%BC%89.html)
## 命令如下：
```
ollama run deepseek-r1:671b
```
> 671b可自行更改为deepseek模型版本如70b，32b，14b，8b，4b，1.5b。
* 此时，ollama会自行下载安装模型并运行。
我们让其自行部署
* 下载[Chatbox](https://chatboxai.app/zh)
* 在模型部署完后打开Chatbox，弹出中选择**使用自己的 API Key 或本地模型**
* 找到ollama API 并选择
* 选择下载的模型并保存
* 新建对话集合使用！
# seepseek部署完成！
快去试试吧~~
