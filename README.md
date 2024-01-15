<h1 align="center"><a href="https://www.hestiacp.com/">Hestia Control Panel</a></h1>

![HestiaCP Web Interface screenshot](https://storage.hestiacp.com/hestiascreen.png)

<h2 align="center">适用于现代网络的轻量级且功能强大的控制面板</h2>

<p align="center"><strong>Latest stable release:</strong> Version 1.8.10 | <a href="https://github.com/hestiacp/hestiacp/blob/release/CHANGELOG.md">View Changelog</a></p>

<p align="center">
	<a href="https://www.hestiacp.com/">HestiaCP.com</a> |
	<a href="https://docs.hestiacp.com/">Documentation</a> |
	<a href="https://forum.hestiacp.com/">Forum</a>
	<br/><br/>
	<a href="https://drone.hestiacp.com/hestiacp/hestiacp">
		<img src="https://drone.hestiacp.com/api/badges/hestiacp/hestiacp/status.svg?ref=refs/heads/main" alt="Drone Status"/>
	</a>
	<a href="https://github.com/hestiacp/hestiacp/actions/workflows/lint.yml">
		<img src="https://github.com/hestiacp/hestiacp/actions/workflows/lint.yml/badge.svg" alt="Lint Status"/>
	</a>
</p>

## **Welcome!**

Hestia 控制面板旨在为管理员提供易于使用的 Web 和命令行界面，使他们能够从一个中央仪表板快速部署和管理 Web 域、邮件帐户、DNS 区域和数据库，而无需手动部署和配置各个组件的麻烦或服务。

## Donate

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ST87LQH2CHGLA)<br /><br />
Bitcoin : bc1q48jt5wg5jaj8g9zy7c3j03cv57j2m2u5anlutu<br>
Ethereum : 0xfF3Dd2c889bd0Ff73d8085B84A314FC7c88e5D51<br>
Binance: bnb1l4ywvw5ejfmsgjdcx8jn5lxj7zsun8ktfu7rh8<br>
Smart Chain: 0xfF3Dd2c889bd0Ff73d8085B84A314FC7c88e5D51<br>

特色与服务
Apache2 和 NGINX 与 PHP-FPM
多个 PHP 版本（5.6 - 8.2、默认 8.1）
具有集群功能的 DNS 服务器（绑定）
具有防病毒、反垃圾邮件和 Webmail 功能的 POP/IMAP/SMTP 邮件服务（ClamAV、SpamAssassin、Sieve、Roundcube）
MariaDB/MySQL 和/或 PostgreSQL 数据库
Let's Encrypt 使用通配符证书支持 SSL
具有暴力攻击检测和 IP 列表（iptables、fail2ban 和 ipset）的防火墙。
支持的平台和操作系统
Debian： 12、11 或 10
Ubuntu： 22.04 LTS、20.04 LTS
笔记：

Hestia 控制面板不支持 32 位操作系统！
Hestia 控制面板与 OpenVZ 7 或更低版本结合使用可能会出现 DNS 和/或防火墙问题。如果您使用虚拟专用服务器，我们强烈建议您使用基于 KVM 或 LXC 的服务器！
安装 Hestia 控制面板
注意：您必须在全新操作系统安装之上安装 Hestia 控制面板，以确保功能正常。
虽然我们已尽一切努力使安装过程和控制面板界面尽可能友好（即使对于新用户），但假设您在之前对如何设置 Linux 服务器的基础知识有一些了解和了解继续。

第 1 步：登录
要开始安装，您需要以root或具有超级用户权限的用户身份登录。您可以直接从命令行控制台或通过 SSH 远程执行安装：

ssh root@your.server
第2步：下载
下载最新版本的安装脚本：

wget https://raw.githubusercontent.com/hestiacp/hestiacp/release/install/hst-install.sh
如果由于 SSL 验证错误而导致下载失败，请确保您已在系统上安装了 ca 证书包 - 您可以使用以下命令执行此操作：

apt-get update && apt-get install ca-certificates
第三步：运行
要开始安装过程，只需运行脚本并按照屏幕上的提示操作即可：

bash hst-install.sh
您将在安装期间指定的地址（如果适用）收到一封欢迎电子邮件，并在安装完成后收到屏幕上的说明，用于登录和访问您的服务器。

自定义安装
您可以在安装过程中指定许多不同的标志，以仅安装您需要的功能。要查看可用选项的列表，请运行：

bash hst-install.sh -h
或者，您可以使用https://hestiacp.com/install.html，它允许您通过 GUI 轻松生成安装命令。

如何升级现有安装
新安装的 Hestia 控制面板默认启用自动更新，并且可以通过服务器设置 > 更新进行管理。要手动检查并安装可用更新，请使用 apt 包管理器：

apt-get update
apt-get upgrade
问题和支持请求
如果您在使用 Hestia 控制面板时遇到一般问题并需要帮助，请访问我们的论坛以搜索潜在的解决方案或发布新帖子以供社区成员提供帮助。
Bug 和其他可重现的问题应通过创建新的问题报告通过 GitHub 提交，以便我们的开发人员可以进一步调查。请注意，支持请求将被重定向到我们的论坛。
重要提示：我们无法为未描述已执行的故障排除步骤的请求或与 Hestia 控制面板无关的第三方应用程序（例如 WordPress）提供支持。请确保您在论坛帖子或问题报告中包含尽可能多的信息！

贡献
如果您想为该项目做出贡献，请阅读我们的贡献指南，以简要概述我们的开发流程和标准。

版权
“Hestia 控制面板”、“HestiaCP”和 Hestia 徽标均为 hestiacp.com 的原始版权，并适用以下限制：

您可以：

在与应用程序或项目直接相关的任何上下文中使用名称“Hestia 控制面板”、“HestiaCP”或 Hestia 徽标。这包括应用程序本身、本地社区以及新闻或博客文章。
您不得：

以“Hestia Control Panel”、“HestiaCP”或类似衍生品的名义出售或重新分发应用程序，包括在与创收活动相关的任何品牌或营销材料中使用 Hestia 徽标，
在与项目无关的任何上下文中使用名称“Hestia Control Panel”、“HestiaCP”或 Hestia 徽标，
以任何方式更改名称“Hestia Control Panel”、“HestiaCP”或 Hestia 徽标。
执照
Hestia Control Panel 根据GPL v3许可证获得许可，并且基于VestaCP项目。
