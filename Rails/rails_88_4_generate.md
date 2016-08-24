
# rails generate関連

参考：[railsコマンド](http://railsdoc.com/rails)
　  
- - - 
## テーブル作成時
```

```
　  
- - - 
## テーブルがすでにある時
[基本的なカラムの追加、削除、変更](http://qiita.com/Kaki_Shoichi/items/077d0a282255cd92cff3)

### 外部キーのカラム追加
bundle exec rails g migration Addカラム名RefToテーブル名 user:references（外部キーの追加：_idは記載しない）  
参考：[外部キー周りの注意](http://b.pyar.bz/blog/2014/10/22/foreigner/)
```
bundle exec rails g migration AddUserRefToTweets user:references
```

### カラムの削除（外部制約も外す）
```
bundle exec rails g migration Removeカラム名Fromテーブル名 カラム名:references
```




### マイグレーション実行
```
bundle exec rake db:migrate
```