
## anbox已经停滞，架构也过于成旧，[WayDroid](https://github.com/WayDroid)更有关注意义


## README
说明与更改记录

这里只是旧版本anbox的相关修改，针对ubuntu 16.04 和 ubuntu touch（测试：米6 halium-7.1），落后于主干仓库

这里为ubuntu旧版本编译，做一些自用性修改、维持低版本编译依赖（其实主仓库调整编译参数也可以为ubuntu xenial编译）



#### 将要做的：
- ubuntu上图像旋转不正确
- ubuntu上不能完成视频拍摄
- webview修复实现修改（现在虽然可用但感觉不是最好的修改）
- ubuntu touch 摄像头初始化适配
- 录音支持修复


#### 已完成的：
- webview初步修复可用，webview shell 已经可用打开网页，ubuntu touch中微信已可使用webview
- 自己打包ubuntu touch 所用android.img ,解包搞出修改项，主干直接打包设备权限差异（操作无响应）和网络不可用
- 合并 alecbarber/anbox 仓库摄像头支持相关修改，ubuntu可以使用摄像头
- 学习/测试 ubuntu touch 调用摄像头
