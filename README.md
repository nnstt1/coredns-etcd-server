# coredns-etcd-server

CoreDNS と etcd で DNS サーバを構築する Playbook です。
（etcd はまだ構築できません）

## 使い方

'inventory' を編集してから 'coredns-etcd-server.yml' を実行してください。

'''bash
ansible-playbook -i inventory coredns-etcd-server.yml -K
'''

## 変数

'inventory' には以下の変数を設定してください。

- domain
- coredns_version
- etcd_server
- etcd_port
