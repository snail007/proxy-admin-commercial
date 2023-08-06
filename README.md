# About ProxyAdmin
ProxyAdmin is a powerful web console of [snail007/goproxy](https://github.com/snail007/goproxy) .

<hr>

[Manual](https://snail.gitee.io/proxy/manual/) ｜ [中文简介](/README_ZH.md) ｜ [参考手册](https://snail.gitee.io/proxy/manual/zh/)

## Preview

### HTTP(S) Proxies
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/http_en.gif)

### Socks5 Proxies
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/socks5_en.gif)

### Internal NAT
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/nat_en.gif)

### Remote Desktop - VNC & Web-SSH
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/rdp.gif)

### DIY Service
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/diy_en.gif)

### Client Arguments
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/client_args.gif)

### View Logging
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/logging.gif)

### Debug Mode
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/debugging.gif)

### Full Demo
![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/demo_cn.gif)

## Start Using

### Quick Installation

If your VPS is a Linux 64-bit system, you only need to execute the following sentence to complete the automatic installation and configuration.

Tip: All operations require root privileges.

```shell
bash -c "$(curl -s -L https://raw.githubusercontent.com/snail007/proxy-admin-commercial/master/install_auto.sh)"
```

The installation is complete, the configuration directory is /etc/gpa. For more detailed usage, please refer to the manual directory above to learn more about the features you want to use.

If the installation fails or your vps is not a linux64-bit system, follow the manual installation steps below.
  
### Manual Installation

Select the file that is appropriate for your system and download it, [click to download](https://github.com/snail007/proxy-admin-commercial/releases)

### Linux && MacOS

The root account is executed:

`cd Enter "proxy-admin directory".

`./proxy-admin install`


### Windows

1. Install using the assistant tool

The administrator opens goproxy_helper.exe and can install/uninstall/restart the service with one click.

![](https://mirrors.host900.com/https://github.com/snail007/proxy-admin-commercial/blob/master/res/images/gh.png)

2. Command line installation

The administrator account executes cmd.exe

`cd Enter "proxy-admin directory".

`proxy-admin.exe install`

### Access

After the installation is successful, open the browser to access: http://127.0.0.1:32080, the first default account is root, the password is 123, remember to modify the first time after login.

Configuration file path:

Linux && MacOS is located in /etc/gpa/app.toml

Windows is located at C:\gpa\app.toml

You can configure the listening port and logging.

## Uninstalling services

### Linux && MacOS

The root account is executed:

`cd Enter "proxy-admin directory".

`./proxy-admin uninstall`


### Windows

The administrator account executes cmd.exe

`cd Enter "proxy-admin directory".

`proxy-admin.exe uninstall`

## Service Management

The following operations must be done before the service is installed.

There are two ways to manage services:

1. Use the program proxy-admin to manage the service.

proxy-admin install install as system service

proxy-admin uninstall uninstall service

proxy-admin start

proxy-admin stop

proxy-admin restart

proxy-admin backup     backup data

proxy-admin restore    restore data

2. Manage using system service management tools.

The proxy-admin system service name is: proxyadmin

Linux can be managed by systemctl.

MacOS can be managed by commands below.

Windows can be managed using the system's Service Manager.

## HTTP API

The control panel defaults to the verification code login mode for the login.
You can also enable the token mode in the configuration file, so that the login can
support verification code and token mode at the same time. Using the token mode,
you can easily simulate the login panel, and then your program can be accessed through http.
It can operate data like on the panel, and can also realize functions that are not
available in the background, such as batch import, start, stop and other operations.

Steps to enable token mode

1.Modify the control panel configuration file app.toml, under [login]

```ini
enable_token=true
token="xxx"
```  

Tips: `xxx` is a specific token, it should be set as a private string of English numbers,
the length is not limited, about 32 are recommended.

2.When requesting the login interface

1. You need to set an HTTP header: `X-Requested-With: XMLHttpRequest`, so that you can log in normally.
2. In addition to the username and password, the login form data also needs a `token` field, and the value is the token
   set in [login] in the configuration file.

3.To operate the data of a certain function of the panel, please use the Chrome browser to open the developer tool,
observe the corresponding interface of the panel operation, and request the form data field.

## UPDATE

### Linux

```shell
proxy-admin update
```

Force update.

```shell
proxy-admin update -f
```

### Windows

```bat
c:\
cd gpa
proxy-admin update
```

Force update.

```shell
c:\
cd gpa
proxy-admin update -f
```

## Thanks

[Back to the light](https://gitee.com/yinqi) The back-end template provided us a comfortable interactive experience.

[GoFrame](https://github.com/snail007/gf) provides a convenient and powerful framework to make the agent backstage development more fluent.
