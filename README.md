# prac_tf

## セットアップ
- AWS IAMにてAdministratorAccessをアタッチしたIAMユーザを作成
- ローカルの~/.aws/config, ~/.aws/credentialsにプロファイルを設定
- awscliのインストール
- tfenvのインストール

### terraformのインストール

**インストール可能なバージョンを取得する**
```
$ tfenv list-remote
0.14.0-alpha20201007
0.14.0-alpha20200923
0.14.0-alpha20200910
0.13.4
...
```

**インストール**
```
$ tfenv install 0.13.4
```

**使用バージョンの選択**
```
$ tfenv use 0.13.4
Switching default version to v0.13.4
Switching completed
```

**ローカルのバージョン取得**
使用中のバージョンには`*`が付く
```
$ tfenv list
* 0.13.4 (set by /usr/local/Cellar/tfenv/2.0.0/version)
```

**.terraform-version**
.terraform-versionに使用バージョンを記述しておくと、`tfenv install`でそのバージョンがインストールされる。

