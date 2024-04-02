# wp-cli-setup-sample

```
wp core language install ja --activate
&& wp option update timezone_string 'Asia/Tokyo'
&& wp option update date_format 'Y-m-d'
&& wp option update time_format 'H:i'
&& wp rewrite structure '/%postname%/'
&& wp option update default_comment_status closed
&& wp theme delete --all --force
&& wp theme install twentytwentyfour
&& wp scaffold _s sample_theme --theme_name="サンプルテーマ" --author="xxxxxx" --author_uri="https://xxxxx.com" --sassify --activate
&& wp plugin install wp-multibyte-patch --activate
&& wp plugin install show-current-template --activate
&& wp plugin install query-monitor --activate
&& wp option update show_on_front 'page'
&& wp option update page_on_front $(wp post create --post_type=page --post_title="フロントページ" --post_status=Publish --porcelain)
&& wp post delete 1 2 3 --force
&& wp core language update 
```

- 日本語をアクティベート
- タイムゾーンを東京に
- 日付フォーマットを'Y-m-d'に
- 時間フォーマットを'H:i'に
- パーマリンクを設定
- コメント欄を閉鎖
- テーマをすべて削除
- twentytwentyfourをインストール
- _sをインストール・アクティベート
- WP Multibyte Patchをインストール・アクティベート
- Show Current Templateをインストール・アクティベート
- Query Monitorをインストール・アクティベート
- トップページを固定ページに
- 固定ページ・フロントページを作成
- 投稿ページを削除
- 翻訳を更新（最後に行う）
