# Organization
## 概要
Organization とは github の共有アカウント.  
複数プロジェクト管理でき,人数も無制限.  
参加者ごとに権限を設定できる.  
Organization は public/private 両方の Repository を無制限に所有可能.  
機能追加はアップグレードが必要.  
Team という機能では Organization の中にグループを作ることができ,権限の一括管理も可能.
## 手順
やまだや作成  
https://github.com/yamada-ya

1. 作りたいものがある場合、まずはリポジトリを作成する.

![リポジトリ作成場所](https://raw.githubusercontent.com/yamada-ya/documents/main/Git/images/repo.jpg)

# Trouble
## push 時にアクセスエラー
### エラー内容
$ git push
Username for 'https://github.com': ユーザ名   
Password for 'https://ymdhal@github.com': パスワード   
remote: Support for password authentication was removed on August 13, 2021.   
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.  
fatal: Authentication failed for 'https://github.com/yamada-ya/documents.git/'   

### 対応
https://ios-docs.dev/20210813support-for-password/  

Fine-grained personal access tokens Beta だとパーミッションがうまく許可できないため、リンク先と同じ Tokens(classic)で Token 生成.  
git remote set-url origin https://トークン@github.com/yamada-ya/documents.git
