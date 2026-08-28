# LEARNINGS — 041-house

## 2026-08-28 明るい部屋化・iOS対応・初公開

- 旧 `3d_house_explorer.html` は暗い夜の部屋＋PC操作（WASD/マウス/Pointer Lock）のみ。小学生向けには操作が難しすぎた。
- ビジュアルを刷新: クリーム壁・木目床・昼光・寝室に勉強机・窓光。ゴール文言を「散らばった大切なもの6個」に統一。
- iOS: `index.html` 新設。仮想十字キー、右半分ドラッグ視点、⏸、タップ開始、WebAudio unlock、safe-area、ダブルタップ防止。
- ハーネス対策: 操作ボタンを DOM 先頭の canvas より前に配置（`button, canvas`.first() が minimap/gameCanvas を誤タップしないよう順序調整）。`bindTap` は click 併用で Playwright tap 互換。
- Three.js 影を無効化しモバイル DPR 1.0 で描画負荷を下げ、RAF 47/秒で harness PASS。
- 初回 GitHub 公開。
