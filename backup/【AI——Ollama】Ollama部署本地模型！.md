
# 前言
## 什么是Ollama？
> Ollama 是一款开源工具，专注于在本地计算机上简化大型语言模型（LLM）的部署与交互。用户可通过命令行直接下载、运行和管理多种模型（如 Llama、Mistral 等），无需依赖云端服务，保障数据隐私。支持 macOS 和 Linux 系统，提供模型微调接口，便于开发者定制化应用。其轻量级架构优化了资源占用，降低硬件门槛，适合研究、实验及开发场景，助力用户高效探索 AI 文本生成、问答等任务，是本地化运行 LLM 的便捷解决方案。
> [其他参考视频](https://www.bilibili.com/video/BV1QtNmeoEe3?vd_source=0957d3bb7550711acd815f905c37e537)
**一款AI模型类软件，我们这里选用Ollama部署本地模型。**
# 部署设置
* 安装 Ollama 软件包
官网地址：https://ollama.com/download
***
## 部署Ollama
* 在 d 盘创建 ollama 文件夹，把软件包放进去
* 以管理员身份，打开CMD命令行窗口
* win + r  弹出窗口
* 输入 cmd  后， ctrl + shift + 回车
* 切换到 d 盘，添加系统环境变量
```
 d: 
 setx OLLAMA_MODELS  d:\ollama /M
```
* 切换到 ollama 目录，清屏（cls），安装ollama程序并指定目录
```
cd ollama
cls
ollamaSetup.exe  /dir=d:\ollama
```
在弹出的安装界面中，点 Install 后， 等待完成
**关闭原来的 CMD，打开一个新的 CMD，查看ollama是否安装成功**（以确保配置成功！不然模型将无法正常下载到d盘！）
```
ollama -v
```
***
## 部署模型
到官网搜索想要的大模型
https://ollama.com
或者点 models 菜单， 或者在搜索框中输入要搜索的名称
找到模型后，查看详情
选择想要的大小尺寸，复制下方的命令
回到 CMD 窗口，粘贴命令

```
ollama pull deepseek-r1:1.5b
```
（将模型下载到本地）
> (下载速度变慢，可以 ctrl+c 中断，过一会再执行 ollama pull deepseek-r1:1.5b, 将会接着上一次的进度进行拉取下载)
***
# 运行大模型
```
ollama run deepseek-r1:1.5b
```
在 >>> 后输入 你好， 即可聊天

结束对话，退出.  或 ctrl + d 退出.
```
/bye
```  
***
### 查看更多相关命令
```
ollama -h  
``` 
***
# UI界面
> 使用ChatBox软件，地址：https://chatboxai.app/zh
* 在模型部署完后打开Chatbox，弹出中选择**使用自己的 API Key 或本地模型**
* 找到ollama API 并选择
* 选择下载的模型并保存
* 新建对话并使用！
#  部署完成~~

