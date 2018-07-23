## 実行環境

- Python 3.6.4

## 手順

- クローン

```
git clone git@github.com:youichiro/message-app.git
cd message-app
```

- データベースの作成

```
mysql -u root -p
> create database message_app;
```

- 必要なライブラリのインストール

```
pip install -r requirements.txt
```

- コンフィグファイルの作成

```
cp message_app/config.py.example message_app/config.py
# message_app/config.pyにデータベースの情報を記入する
```

- マイグレーション

```
python manage.py makemigrations
python manage.py migrate
```

- 起動

```
python manage.py runserver
# localhost:8000/view/を開く
```