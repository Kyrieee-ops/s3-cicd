# s3-cicd deploy command
aws cloudformation deploy \
--stack-name s3-cicd-stack \
--template-file s3-cicd.yml \
--capabilities CAPABILITY_NAMED_IAM \
--profile Administrator


# GitHub OAuthトークンを発行する
以下`GitHub Developers Settings`のページにてトークンを発行する
https://github.com/settings/tokens

`Generate new token`を選択する。
![Generate new tokun Beta](./img/Generate%20new%20token.png)

`Use GitHub Mobile`を使用してGitHubにサインインする。
![Use GitHub Mobile](./img/Confirm%20access.png)

`New fine-grained personal access token`画面にて一意のトークン名を指定し、トークンを発行する。
トークンの名前は用途がわかりやすい名前にすると良い。
今回は`CodePipeline-GitHub-Access`のようにしてみます。
![Create access token](./img/Token.png)

Repository accessはセキュリティを考慮して`Only select repositories`を選択し、特定のリポジトリのみアクセスが必要な場合を選択します。
![Repository access](./img/Repository%20access.png)