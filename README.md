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

### init, plan, apply
リソース定義を記述したファイル(.tf)のある場所で`terraform init`を叩くと、ローカルのterraform環境が初期化される。  
`terraform plan`で実行計画を出力。何が作られるか、削除されるか、更新されるかなどが出力対象。 
`terraform apply`で実行計画を適用する。planの内容が表示され、実行確認が入るので、'yes'を入力すると実行される。

