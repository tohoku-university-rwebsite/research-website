# 東北大学某研究室のWebサイトを作る
以下のコマンドを実行するとdockerの環境が立つ（初回のみ）
```
git clone https://github.com/tohoku-university-rwebsite/research-website.git
docker-compose build
docker-compose up -d
docker-compose run web rails webpacker:install
docker-compose run web rails webpacker:install:vue
docker-compose run web bin/webpack
docker-compose run web rake db:create
```

2回目以降は以下のコマンドで環境が立つはず
```
docker-compose up -d
docker-compose run web bin/webpack
```

dockerの環境が立ったら、ブラウザで`http://localhost:3000`にアクセス

- 参考サイト
  - [Docker for MacでRails5.1+Vue.jsの環境をサクッと構築](https://terakoya.site/dev/docker-mac-rails51-vuejs-setup/)
