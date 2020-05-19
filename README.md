# About ProxyAdmin
ProxyAdmin is a powerful web console of [snail007/goproxy](https://github.com/snail007/goproxy) .

<hr>

[中文简介](/README_ZH.md)

[snail007/goproxy manual](https://snail007.github.io/goproxy/manual/#/)

## Preview

### HTTP(S) Proxies
![](/res/images/http_en.gif)

### Socks5 Proxies
![](/res/images/socks5_en.gif)

### Internal NAT
![](/res/images/nat_en.gif)

### Remote Desktop - VNC & Web-SSH
![](/res/images/rdp.gif)

### DIY Service
![](/res/images/diy_en.gif)

### Client Arguments
![](/res/images/client_args.gif)

### View Logging
![](/res/images/logging.gif)

### Debug Mode
![](/res/images/debugging.gif)

### Full Demo
![](/res/images/demo_cn.gif)

## Start Using

### Quick Installation

If your VPS is a Linux 64-bit system, you only need to execute the following sentence to complete the automatic installation and configuration.

Tip: All operations require root privileges.

```shell
curl -L https://raw.githubusercontent.com/snail007/proxy-admin-commercial/master/install_auto.sh | bash
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

![](/res/images/gh.png)

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

2. Manage using system service management tools.

The proxy-admin system service name is: proxyadmin

Linux can be managed by systemctl.

MacOS can be managed by commands below.

Windows can be managed using the system's Service Manager.

## Thanks

[Back to the light](https://gitee.com/yinqi) The back-end template provided us a comfortable interactive experience.

[GoFrame](https://github.com/gogf/gf) provides a convenient and powerful framework to make the agent backstage development more fluent.