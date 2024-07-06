# MlabHP

## セットアップ
```bash
# 1. sailのエイリアスの設定（設定しない場合はそれぞれのコマンドを./vendor/bin/sailに読み替える）
vim ~/.zshrc
alias sail="./vendor/bin/sail"
source ~/.zshrc

# 2. envをコピー　/　書く環境に合わせて編集
cp .env.example .env

# 3. sailでDockerコンテナの起動
sail up -d

# 4. アプリケーションキーを生成
sail composer install
sail artisan key:generate
```

## GitHub Actions(GA)について
workflow（テスト等）を自動化してくれるサービス  
今回は「mainにpushした時 or PRした時」にテストを行うように設定しています