# daily-site

[daily.horatio.cn](https://daily.horatio.cn) 的落地页——「日记系列」两款 Android 应用（[热量日记](https://github.com/HoratioShaw/calorie-diary)、[开支日记](https://github.com/HoratioShaw/expense-diary)）的下载入口。

单文件静态页 `index.html`（CSS 内联，无构建步骤、无外部资源），推送到 `main` 即由 self-hosted runner rsync 部署到服务器 `/www/wwwroot/daily.horatio.cn/`。

- 部署流程：`.github/workflows/deploy.yml`，机密见仓库 Secrets（`SERVER_HOST` / `SERVER_USER` / `SERVER_SSH_KEY`）。
- 面板与证书文件（`.user.ini` / `.htaccess` / `.well-known`）永不传输、永不删除；部署不使用 `--delete`。
