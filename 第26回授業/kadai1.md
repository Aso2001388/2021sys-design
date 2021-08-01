# DB定義書
## ER図
[ER図はこちら(申し訳ありません。作成してないです)]()

# DBテーブルカラム詳細一覧

**購入テーブル(d_purchase)**
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|オーダーID|order_id|int(80)|○|○||
|顧客コード|customer_code|varchar(80)||○||
|購入日|purchase_date|date||○||
|支払ID|payment_id|int(10)||○|○|
|配達ID|delivery_id|int(10)||○|○|

**購入詳細テーブル(d_purchase_detail)**
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|オーダー詳細ID|detail_id|int(80)|○|○||
|オーダーID|order_id|int(80)|○|○|○|
|商品コード|item_code|int(11)||○|○|
|価格|price|int(11)||○||
|数量|num|int(11)||○||

**顧客マスタ(m_customers)**
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|顧客コード|customer_code|varchar(80)|○|○||
|パスワード|pass|varchar(50)|○|○||
|メールアドレス|mail|vachar(100)||○||
|住所|address|varchar(200)||○||
|電話番号|tel|varchar(20)||○||
|郵便番号|Pastalcode|varcher(20)||○||
|国籍|kokuseki|varcher(50)||○||


**カテゴリマスタ(m_category)**
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|カテゴリID|category_id|int(11)|○|○||
|カテゴリ名|name|varchar(20)||○||
|登録日|reg_date|date||○||

**商品マスタ(m_items)**
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|商品コード|item_code|int(11)|○|○||
|商品名|item_name|varchar(50)||○||
|価格|price|int(11)||○||
|カテゴリID|category_id|int(11)||○|○|
|画像ファイル名|image|varchar(200)||○||
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||○||
