---
title: RaspberryPiでProxy設定をする
tags:
    - RaspberryPi
    - Proxy
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: false
---

# Raspberry Pi で Proxy 設定をする

Raspberry Pi で Proxy 設定をする方法をまとめます．

## 各種設定ファイルの編集

```bash:/etc/apt/apt.conf.d/apt.conf
Acquire::http::Proxy "http://proxy.example.com:8080/";
Acquire::https::Proxy "http://proxy.example.com:8080/";
Acquire::ftp::Proxy "http://proxy.example.com:8080/";
Acquire::socks::Proxy "http://proxy.example.com:8080/";
```

```bash:/etc/environment
http_proxy=http://proxy.example.com:8080/
https_proxy=http://proxy.example.com:8080/
ftp_proxy=http://proxy.example.com:8080/
```

```bash:~/.bashrc
export http_proxy=http://proxy.example.com:8080/
export https_proxy=http://proxy.example.com:8080/
export ftp_proxy=http://proxy.example.com:8080/
```

完了．
