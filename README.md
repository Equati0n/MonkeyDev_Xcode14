# MonkeyDev_Xcode14

MonkeyDev 支持Xcode 14安装  
修复Xcode14 MacOSX Package Types.xcspec not found报错

```
Summit ~ % cd MonkeyDev/bin

执行安装命令
Summit bin % sudo bash md-install

Password:
Downloading MonkeyDev base from Github...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 3452k  100 3452k    0     0   884k      0  0:00:03  0:00:03 --:--:--  885k
Downloading Xcode templates from Github...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  306k  100  306k    0     0   333k      0 --:--:-- --:--:-- --:--:--  335k
Downloading frida-ios-dump from Github...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  9669  100  9669    0     0   2417      0  0:00:04  0:00:03  0:00:01  2420
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 11727  100 11727    0     0   4523      0  0:00:02  0:00:02 --:--:--  4533

安装完成
Creating symlink to Xcode templates...
Modifying Bash personal initialization file...

Summit bin % 
```
# 运行遇到的报错

### “error: Signing for “SummitDylib” requires a development team.”
### “Select a development team in the Signing & Capabilities editor.”

在Xcode中 选中Dylib对应的target (in target ‘SummitDylib’)

点击Build Settings 中  在User-Defined (用户自定义那一栏)

添加"CODE_SIGNING_ALLOWED = NO" 关闭对Dylib的Code签名


# libstdc++
`Xcode 10`之后删除的`libstdc++`库

1. 先下载下来这个项目，然后打开终端`cd`到`libstdc--master`文件夹；
2. 如果你使用的是 Xcode 10，则将`install-xcode_10.sh`拖到终端中执行即可；
3. Xcode 11 之后的版本则将`install-xcode_11+.sh`拖到终端中执行。

## iOS file not found: /usr/lib/libstdc++.dylib
```

~ % cd /Users/Summit/libstdc- 

~ % sudo sh install-xcode_11+.sh
```
