# SPEC — 041-house『おうち探検』

- 対象ゲーム: `041-house`
- 作成日: 2026-08-28
- 更新日: 2026-08-28
- ステータス: 公開
- 参照ファイル: `index.html`

## 1. ゲーム概要

- ジャンル: 3D一人称・おうち探索
- 一言説明: 明るい6部屋の家を歩き回り、散らばった大切なもの6個を集める
- 想定プレイ時間: 3〜5分
- 想定プレイヤー: 小学生〜。iPhone Safari 片手操作
- クリア体験: 6個全部見つけて「お片付け完了！」

## 2. 対象環境

### 必須
- 配信先: GitHub Pages
- 最優先端末: iPhone Safari
- 対応画面幅: 320px〜430px
- 実装: 静的 HTML + Three.js（CDN r128）

### 任意
- PC: WASD / 矢印 + マウス（Pointer Lock）

### 未確定
- 6個のアイテム具体名（宿題ノート等への差し替えは将来対応）

## 3. 操作

| 端末 | 移動 | 視点 | 一時停止 |
|---|---|---|---|
| スマホ | 左下十字キー | 画面右半分ドラッグ | ⏸ボタン |
| PC | WASD / 矢印 | マウス | Esc |

- アイテム取得: 近づくだけ（自動）

## 4. 勝敗条件

- 勝利: コレクタブル6個すべて取得
- 敗北: なし（時間制限なし）

## 5. ファイル構成

```text
041-house/
  index.html
  3d_house_explorer.html  # 旧ファイル（参照用）
  SPEC.md
  LEARNINGS.md
  .nojekyll
```

## 6. 実装制約

- 公開実体 20MB 以下
- iOS: viewport-fit=cover、touch-action、ダブルタップ防止、WebAudio unlock
- 仮想パッド 56px 以上、`setPointerCapture`

## 7. テスト項目

- [x] game-harness PASS（2026-08-28）
- [ ] iPhone 実機プレイ（未）
