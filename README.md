# 越狱插件环境配置
### 安装TheOS
`git clone https://github.com/DHowett/theos $THEOS`
### 安装ldid

```
sudo curl -s http://dl.dropbox.com/u3157793/ldid > /tmp/ldid
sudo cp /tmp/ldid $THEOS/bin/
sudo chmod +x $THEOS/bin/ldid
rm /tmp/ldid
```
### 环境配置
1. 设置环境变量
    export THEOS=/opt/theos
2. 进入你打算放置项目的文件夹
    cd ~/project
3. 创建工程nic.pl
    
```
NIC 2.0 - New Instance Creator
------------------------------
  [1.] iphone/activator_event
  [2.] iphone/application_modern
  [3.] iphone/cydget
  [4.] iphone/flipswitch_switch
  [5.] iphone/framework
  [6.] iphone/ios7_notification_center_widget
  [7.] iphone/library
  [8.] iphone/notification_center_widget
  [9.] iphone/preference_bundle_modern
  [10.] iphone/tool
  [11.] iphone/tweak
  [12.] iphone/xpc_service
```

4. 这里对这五种类型做个简单介绍，application 是创建普通应用程序的，library 是创建库文件，preference_bundle 是创建设置束，tool是开发那种没有界面的，就好像 hello world那种程序的，tweak 就是最精华的部分了，我们这里姑且翻译为外挂程序，关于tweak的开发介绍我打算再单独开一篇文章用来描述。接着，根据提示，分别输入模版类型、工程名、包名、作者名等参数回车，等待初始化完成即可进入工程文件夹，编辑源文件了
5. 可以在.xm文件中编写logos语言修改源代码逻辑
6. make 编译项目工程
7. make package 打包工程
8. make install 载入对应的deb包

### linux、mac的bash和zsh如何切换
chsh -s /bin/bash和chsh -s /bin/zsh可以永久切换，也就是一登录进来的就是相应的界面


