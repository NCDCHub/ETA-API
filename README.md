# ETA-API
ETAのWebサービスAPIの仕様を定義します。

## 原則
- RESTFulなAPIとします。
- カードと異なり、データサイズを小さくすることの優先度は小さいたいめ、TLV構造ではなく、人が読みやすい形で返すこととします。
  - TLV構造のTag名を使うことも考えられる。その方がカードとWeb APIの処理を共通化できるかも知れない。ただｓ、Tag名だとその項目が何を示しているか仕様書を見ながらで無いと、またはETAの仕様に精通した人で無いと分からない  
- httpsを使用することとします。
- 認証方式はプロジェクトによって個別に検討とします
  - で、良いか？決めておいた方が間違い無いので、何かしら決めてるというのも案。

## URL

https://<host>:<port>/<context root>/eta_request/<card number>

## 支援情報の取得

### リクエスト
`GET` メソッド

https://<host>:<port>/<context root>/eta_request/<card number>

### レスポンス

```
language:[AA, BB, CC, DD];
authority:{
  oid:;
  request1:;
  request2:;
  request;[
    {}
    
    ;
  
```


## 支援情報の取得

### メソッド

GET

### リクエスト

### レスポンス
## 支援情報の取得

### メソッド

GET

### リクエスト

### レスポンス

## 支援情報の削除

### メソッド

DELETE

### リクエスト

### レスポンス

