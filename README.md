Vagrant up で CentOS 6.5, 64bit を使う
=============

centos65 という名前をつけて vagrant box (VM のイメージ) を取ってくる。

```
vagrant init centos65 https://github.com/2creatives/vagrant-centos/releases/download/v6.5.1/centos65-x86_64-20131205.box
```
(200 MB ぐらいダウンロードするのでここでコーヒーを飲む。または歯磨きをする)

VM が立ち上がる。
```
vagrant up
```

立ち上がった VM に ssh してみる。

```
vagrant ssh
```

VM を終了する。
```
vagrant halt
```

VM をぶっこわす。
```
vagrant destory
```

## NeXT Step

1. vagrant up と同時に自動的に provisioning してしまう。Chef Solo, Ansible など
2. VirtualBox 以外にも vagrant up する
3. vagrant box add onamae URL でお好きなボックスを追加。URL はここを見て下さい。 http://www.vagrantbox.es
4. config.vm.box_download_checksum して確かめる http://docs.vagrantup.com/v2/vagrantfile/machine_settings.html

