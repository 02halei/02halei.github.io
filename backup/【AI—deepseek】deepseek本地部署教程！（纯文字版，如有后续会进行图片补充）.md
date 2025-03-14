# 出一期deepseek的本地部署教程
> 软件使用：ollama
> 系统：Windows
---
* 首先你需要一个硬件部署，这里我用的机架式服务器。[可参考文章](https://02halei.github.io/post/%E3%80%90-fu-wu-qi-%E3%80%913500-yuan-ji-jia-shi-fu-wu-qi-pao-deepseek671b-mo-xing-xiang-guan-~%EF%BC%88-chun-wen-zi-ban-%EF%BC%8C-ru-you-hou-xu-hui-jin-xing-tu-pian-bu-chong-%EF%BC%89.html)
* 下载[ollama](https://ollama.com/)并运行安装程序。
* win+R打开cmd，输入命令下载模型。
> 注意ollama默认下载在C盘，模型同样，请确保C盘空间足够！[如需更改磁盘请参考文章](https://02halei.github.io/post/%E3%80%90AI%E2%80%94%E2%80%94OLLAMA%E3%80%91Ollama-bu-shu-ben-di-mo-xing-%EF%BC%81%EF%BC%88-bian-xie-zhong-%EF%BC%89.html)
命令如下：
ollama run deepseek-r1:671b
> 671b可自行更改为deepseek模型版本如70b，32b，14b，8b，4b，1.5b。
* 此时，ollama会自行下载安装模型并运行。
我们让其自行部署
* 下载[Chatbox](https://chatboxai.app/zh)
* 在模型部署完后打开Chatbox，弹出中选择**使用自己的 API Key 或本地模型**
* 找到ollama API 并选择
* 选择下载的模型并保存
* 新建对话集合使用！
## seepseek部署完成！
