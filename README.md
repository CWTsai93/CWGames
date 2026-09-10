# CWGames

CW 自己做的小遊戲收藏，純前端靜態網頁，用 GitHub Pages 發佈。

公開網址：<https://cwtsai93.github.io/CWGames/>

## 目前收錄

| 遊戲 | 路徑 | 說明 |
| --- | --- | --- |
| 方塊時光 | [`/fangkuai/`](./fangkuai/) | 繁體中文俄羅斯方塊，大按鈕操作、速度可選、可離線遊玩 |

## 檔案結構

```
CWGames/
├── index.html          ← 遊戲目錄首頁
├── README.md
└── fangkuai/           ← 方塊時光（單一頁面 PWA）
    ├── index.html
    ├── manifest.webmanifest
    ├── sw.js
    └── icon-*.png / apple-touch-icon.png / favicon-32.png
```

## 發佈設定

Settings → Pages → Source：`Deploy from a branch`，Branch `main`、資料夾 `/ (root)`。

推上 `main` 之後約 1–2 分鐘自動更新。

## 之後要再加一個遊戲

1. 在根目錄開一個新資料夾（例如 `sudoku/`），裡面放該遊戲的 `index.html`
2. 打開根目錄的 `index.html`，複製 `<li class="game-item">` 那整段，改成新遊戲的路徑、名稱、說明與圖示
3. commit、push，首頁就會多一張卡片

## 改版注意

改過 `fangkuai/index.html` 後，請把 `fangkuai/sw.js` 最上面的 `VERSION`（`fangkuai-v1`）版本號 +1，否則已加到主畫面的手機會繼續用舊快取。
