# 健活日記 — 全方位健康管理 APP

血壓 / 心率記錄、BMI 追蹤、運動與睡眠紀錄 — **PWA 版本，可安裝、可離線使用**。

> 原始碼由 [Gemini](https://gemini.google.com/) 生成，原始分享對話：
> <https://share.gemini.google/eR6zJRHMHpig>

## 功能

- **血壓與心率記錄** — 收縮壓 / 舒張壓 / 脈搏，含趨勢圖與歷史清單
- **個人資料** — 年齡、性別、身高體重與 BMI 狀態
- **運動紀錄** — 步數與運動資料同步（Fit）
- **睡眠追蹤** — 睡眠時數記錄
- **資料管理** — 匯入 / 匯出備份（JSON）

資料保存在瀏覽器本機，不會上傳任何伺服器。

## PWA

| 項目 | 說明 |
|------|------|
| Manifest | `manifest.webmanifest`（standalone、brand blue 主題、3 種 icon 含 maskable） |
| Service Worker | `sw.js` — app shell cache-first、導航 network-first、靜態 stale-while-revalidate |
| 離線 | ✅ 全部依賴本地化至 `vendor/`，無外部請求 |
| 安裝 | iOS：Safari 分享 → 加入主畫面；Android Chrome：選單 → 安裝應用程式 |

## 開發

```bash
python3 -m http.server 8899   # 需經 HTTP 才能註冊 Service Worker
# → http://127.0.0.1:8899
```

## 技術棧

Tailwind CSS 3（CDN 版，已本地化）· Chart.js · Font Awesome 6.4 · 原生 JS

## License

MIT
