# API リファレンス（shared memory）

## 共通エンドポイント
プロジェクトごとに上書き可能。

### 認証
- Authorizationヘッダ: `Bearer ${API_TOKEN}`
- トークン取得: `POST /auth/token`
- トークン更新: `POST /auth/refresh`

### エラーレスポンス形式
```json
{
  "error": {
    "code": "ERROR_CODE",
    "message": "人間可読みメッセージ",
    "details": {}
  }
}
```

### ステータスコード
- 200: Success
- 400: Bad Request (validation error)
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 409: Conflict
- 500: Internal Server Error

## プロジェクト固有情報
※ 各プロジェクトで上書きして使うこと
