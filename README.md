# coredns-etcd-server

CoreDNS と etcd で DNS サーバを構築する Playbook です。

CoreDNS は公式バイナリ、etcd は公式コンテナを使った systemd によるサービス化をしています。

## 事前準備

Playbook 内で利用する Collections を事前にインストールしてください。

```bash
ansible-galaxy collection install containers.podman
```

## 使い方

`inventory` を編集してから `coredns-etcd-server.yml` を実行してください。

```bash
ansible-playbook -i inventory coredns-etcd-server.yml -K
```

## 変数

`inventory` には以下の変数を設定してください。

- domain
- coredns_version
- etcd_version
- etcd_server
- etcd_port
