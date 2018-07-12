conoha
======

A command-line interface to the ConoHa.  
**conoha** は [ConoHa](https://www.conoha.jp/)
  をコマンドライン上で操作するために作られたCLIツールです。

Requirements
============

Python 3.0

Installation
============

以下のコマンドを実行することで conoha コマンドが利用可能になります。:

    $ pip install conoha

Configuration
=============

以下のコマンドを実行することで初期設定が完了します。:

    $ conoha
    username: XXXX
    password: XXXX
    tenant_id: XXXX
    Authentication success.

| 初期設定を行った内容は \~/.conoha/config にTOML形式で保存されます。
| ※ユーザ情報が登録されているリージョンは自動で判定されます。

Usage
=====

各コマンドには様々なオプションが存在し \--help
オプションで調べることができます。

VM一覧取得:

    $ conoha compute vm list
    $ conoha compute vm list --detail
    $ conoha compute vm list --text

VMプラン一覧取得:

    $ conoha compute flavors list
    $ conoha compute flavors list --detail
    $ conoha compute flavors list --text

イメージ一覧取得(nova):

    $ conoha compute images list
    $ conoha compute images list --detail
    $ conoha compute images list --text

VM作成:

    $ conoha compute vm create -i [IMAGE_ID] -f [FLAVOR_ID] --password [ADMIN_PASSWORD]

VM起動:

    $ conoha compute vm up [VM_ID]

VM再起動:

    $ conoha compute vm reboot [VM_ID]

VM通常停止:

    $ conoha compute vm stop [VM_ID]

VM強制停止:

    $ conoha compute vm stop [VM_ID] --force

License
=======

MIT