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

`https://<host>:<port>/<context root>/eta_request/<card number>`

### 結果
HTTPレスポンスコードを見て結果を判定。
- 200 OK:成功
- 201 Created:データの生成に成功
- 400 Bad Request:クライアントのリクエストが不正
- 401 Unauthorized:未認証
- 404 Not Found:該当のカード番号は登録されていない
- 500 Internal Server Error:サーバー側の内部エラー

エラーの詳細な内容はBodyで返してもいいかも知れない。

## 支援情報の取得

### リクエスト
`GET` メソッド

`https://<host>:<port>/<context root>/eta_request/<card number>`

### レスポンス
HTTPレスポンスコードを見て結果を判定。
成功の場合のBody部として以下が返る。

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


## 支援情報の登録

### リクエスト

`POST`メソッド

### レスポンス
HTTPレスポンスコードを見て結果を判定。

## 支援情報の更新

### リクエスト
`PUT`メソッド


### レスポンス
HTTPレスポンスコードを見て結果を判定。

## 支援情報の削除

### リクエスト
`DELETE`メソッド

`https://<host>:<port>/<context root>/eta_request/<card number>`

### レスポンス
HTTPレスポンスコードを見て結果を判定。
