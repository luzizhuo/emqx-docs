# CentOS/RHEL

本章节将指导您如何在 CentOS/RHEL 系统中下载安装并启动 EMQX。

支持的 CentOS/RHEL 版本：CentOS 7, CentOS 8。

## rpm 安装

1. 下载 [emqx-5.0.13-el8-amd64.rpm](https://www.emqx.com/downloads/broker/v5.0.13/emqx-5.0.13-el8-amd64.rpm)

```bash
wget https://www.emqx.com/downloads/broker/v5.0.13/emqx-5.0.13-el8-amd64.rpm
```

2. 安装

```bash
sudo yum install ./emqx-5.0.13-el8-amd64.rpm -y
```

3. 启动

- 直接启动：

  ```bash
  $ emqx start
  EMQX 5.0.13 is started successfully!

  $ emqx_ctl status
  Node 'emqx@127.0.0.1' 5.0.13 is started
  ```

- systemctl 启动：

  ```bash
  sudo systemctl start emqx
  ```

- service 启动：

  ```bash
  sudo service emqx start
  ```

4. 卸载

  ```shell
  sudo yum remove emqx
  ```

## tag.gz 安装

1. 下载 [emqx-5.0.13-el8-amd64.tar.gz](https://www.emqx.com/downloads/broker/v5.0.13/emqx-5.0.13-el8-amd64.tar.gz)

```bash
wget https://www.emqx.com/downloads/broker/v5.0.13/emqx-5.0.13-el8-amd64.tar.gz
```

1. 解压程序包

```bash
mkdir -p emqx && tar -zxvf emqx-5.0.13-el8-amd64.tar.gz -C emqx
```

3. 启动

```bash
cd emqx && ./bin/emqx start
```