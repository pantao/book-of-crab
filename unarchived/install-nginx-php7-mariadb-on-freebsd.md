# 在 FreeBSD 上安装 Nginx + PHP7 + MariaDB 环境

## 更新 Freebsd Ports Tree

```bash
portsnap fetch update
```

## 安装 PHP 7.x

> 你可以使用 Ports安装 或者 二进制包安装 PHP

### 使用 Ports 安装

从 ports tree 中搜索 `php`

```bash
ls /usr/ports/lang | grep php
```

在我的机器上，输出：

```text
php-mode.el
php56
php56-extensions
php70
php70-extensions
php71
php71-extensions
php72
php72-extensions
php73
php73-extensions
php_doc
```

安装 `php73`

```bash
cd /usr/ports/lang/php73
make install clean
```

漫长的等待，终于安装完成。

### 使用 pkg 安装

```bash
pkg install php73
```