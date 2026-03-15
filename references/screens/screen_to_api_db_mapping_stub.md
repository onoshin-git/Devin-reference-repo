# 画面 -> API -> DB 対応 Stub

これは参考用 stub です。正本ではありません。

## 例

| 画面項目 | API | backend | DB |
|---|---|---|---|
| `login.html.user_id` | `POST /auth/login.user_id` | `login_handler` | `UsersTable.user_id` |
| `login.html.password` | `POST /auth/login.password` | `login_handler` | `UsersTable.password` |
| `index.html.level-lv2` | `GET /levels/status` | `gate_handler` | `ProgressTable.lv1_passed` |
