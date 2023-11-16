---
title: Dockerでsudoがないとき
tags:
    - 'Docker'
private: false
updated_at: '2023年11月16日'
id: null
organization_url_name: null
slide: false
ignorePublish: false
---

# 起こったこと

Docker に vim をインストールしたかったが，sudo がないと怒られた．
未来の自分の備忘録として残しておく．

```bash
$ sudo apt-get install vim
bash: sudo: command not found
```

# 解決策

sudo をインストールする．

```bash
$ apt-get update
$ apt-get install sudo
```

これで無事に sudo が使えるようになり，vim をインストールすることができた．

# 参考

https://qiita.com/TakuyaMiyashita/items/46542a2b94f86a7bc740
