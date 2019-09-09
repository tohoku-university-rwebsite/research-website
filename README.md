# 東北大学某研究室のWebサイトを作る
以下のコマンドを実行するとdockerの環境が立つ
```
git clone https://github.com/tohoku-university-rwebsite/research-website.git
docker-compose up -d
docker-compose run web rake db:create
```
dockerの環境が立ったら、ブラウザで`http://localhost:3000`にアクセス
