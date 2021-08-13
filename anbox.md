

anbox 是一个基于LXC容器技术的 android 虚拟化系统，使用定制版LXC容器(表述可能部准确，依赖liblxc,在内部操作lxc容器)，现在支持 gles2

主干仓库：https://github.com/anbox/anbox，主干仓库现在要求 ubuntu18.04 及以上系统，升级过部分依赖也调整一些 C++ 写法需高版本编译工具编译。

有很多团队在上面做了优化，有的开源，但是有很多修改没合并到主干仓库。主干仓库几乎已停滞，项目维护者或许因职业原因放弃该项目

以下是我关注的

https://gitee.com/openeuler/anbox 国内组织维护的基于 https://github.com/anbox/anbox/tree/56c25f162ce87edb0fd97f9552b0f597b3a62b76

https://github.com/ubports/anbox 针对 ubuntu touch 的修改

https://github.com/sfdroid/anbox 针对旗鱼 OS 的修改，已废弃

https://github.com/alecbarber/anbox 为 anbox 做 camera 支持，第一个有 camera 支持的仓库，未合并主干。

https://gitee.com/anbox/anbox-headless 支持非 SDL 显示输出以提高显示流畅度

xdroid 不承认是基于 anbox，群里提 anbox 会被踢，提供 gles3 支持： https://www.linzhuotech.com

有反编译过其中一个依赖库文件libxdroid-share.so，可以看出类和函数是重命名把所有 anbox 改成了 xdroid，类名，函数名，错误信息以及调试输出信息。也把其中的几个简单脚本搞成了加密的非脚本语言实现。

不过由于anbox核心编译后非常小，非静态编译结果仅几兆，这个重命名anbox的依赖库文件仅占xdroid打包程序（接近 1G 文件，主程序 + 各种依赖库 +android.img）中的极小部分，xdroid 为 anbox 做了个好用的管理工具，软件仓库工具，用 qt 做的。这个很小的 so 也是 xdroid 的核心所在。

也有其他基于 anbox 的商业化项目，包括华为等多个公司都有对应产品，不关注就不找链接了，不清楚是否开放修改后的源码。

https://github.com/WayDroid 新架构的anbox，使用标准LXC容器。
现阶段是为 ubuntu touch 做，要求是必须是基于halium-9或更高版本适配的ubuntu touch才能使用
也在ubuntu desktop上运行良好

还有一个是基于 qemu 的类似 libhoudini 的实现，用于在 x86 上跑 arm 的 app 的东西：
https://github.com/goffioul/ax86-nb-qemu-guest
https://github.com/goffioul/ax86-nb-qemu-qemu
https://github.com/goffioul/ax86-nb-qemu


