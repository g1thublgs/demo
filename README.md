# note
## [vscode离线安装插件方法](https://blog.csdn.net/Strive_For_Future/article/details/126152498)

## [vscode官网插件下载地址](https://marketplace.visualstudio.com/vscode)

## [vscode-python插件](https://github.com/microsoft/vscode-python/releases)

## google 翻译 
- cmd(管理员)输入：
```
echo 142.250.4.90 translate.googleapis.com >> C:\Windows\System32\drivers\etc\hosts & ipconfig /flushdns > nul
```
- 142.250.4.90（截至2023.01.03可用） 

## [计算机自学指南](https://github.com/PKUFlyingPig/cs-self-learning)

## python 错误大全
- [python 解决Fatal error in launcher:错误问题](https://www.jb51.net/article/187013.htm)

## python 国内镜像
```
python -m pip install xxx -i https://pypi.tuna.tsinghua.edu.cn/simple
```
- [阿里云](https://mirrors.aliyun.com/pypi/simple/)
- [豆瓣](https://pypi.douban.com/simple/)
- [清华大学](https://pypi.tuna.tsinghua.edu.cn/simple/)
- [中国科学技术大学](https://pypi.mirrors.ustc.edu.cn/simple/)
- [华中科技大学](https://pypi.hustunique.com/)

## python 离线安装第三方库
- [呕心沥血整理，python离线安装第三方库（带疑难杂症实例）！！！](https://www.iotword.com/4045.html)
- [python如何离线安装第三方库 ](https://blog.51cto.com/u_15477333/4925660)
- [window下python怎么离线安装tar.gz](https://jingyan.baidu.com/article/ceb9fb1011c41cccad2ba0e9.html)
## [python 删除所有第三方库](https://blog.csdn.net/LM813381916/article/details/127787047)

## [Markdown编辑器-2022最新Typora破解激活教程](https://baijiahao.baidu.com/s?id=1740851053333949382&wfr=spider&for=pc)

## jupyter nbextensions 下载安装
```
python -m pip install jupyter_contrib_nbextensions -i https://pypi.tuna.tsinghua.edu.cn/simple/
```
启动jupyter notebook出现nbextensions插件不显示问题，运行以下代码
```
python -m jupyter nbextensions_configurator enable
```
确保以上两个库（jupyter_contrib_nbextensions和jupyter_nbextensions_configurator）安装完毕之后，执行以下代码安装 javascript and css files
```
python -m jupyter contrib nbextension install --user
```
## 离线批量安装python第三方库
- 1.在有网电脑上参照有互联网环境下安装库的步骤，安装你所需要的库。
```
python -m pip install xxx -i https://pypi.tuna.tsinghua.edu.cn/simple/
```
- 2.将安装的库导出为文本文件，文本中字母后面的数字是版本号，不用删掉
```
python -m pip freeze req.txt
```
- 3.编辑 req.txt ，只保留需要导出的库名称
- 4.将req.txt里面列出的库文件下载到pkg目录
```
python -m pip download -r req.txt -d pkg -i https://pypi.tuna.tsinghua.edu.cn/simple/
```
- 5.U盘转移文件，使用U盘从有网电脑上，将exp 文件夹 （内含 req.txt 和 pkg 文件夹）复制到无网电脑。
- 6.在无网电脑上执行下面命令来安装库，在exp文件夹中右键打开CMD窗口
```
python -m pip install --no-index --find-links=pkg -r req.txt
```
