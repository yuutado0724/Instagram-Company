# Instagram Company Context

このファイルは、新しいCodexスレッドで作業を再開するための引き継ぎメモです。

## 現在の目的

Instagram運用を自動化する会社組織をCodex内に作る。テーマは「AI x 副業 x インスタ運用」。各部署が `AGENT.md` の会社全体ルールを参照しつつ、部署別 `AGENTS.md` に沿って作業する構成にしている。

## リポジトリ

- ローカル: `C:\Users\yuuta\Desktop\instagram-company`
- GitHub: `https://github.com/yuutado0724/Instagram-Company`
- ブランチ: `main`
- すでに初回push済み。
- その後に追加・修正したルール類は未コミットの可能性があるため、再開時はまず `git status --short` を確認する。

## 重要ファイル

- `AGENT.md`: 会社全体の共通ルール。各部署が参照する最上位ルール。
- `AGENTS.md`: Codex向けの入口ルール。作業時に `AGENT.md` と部署別 `AGENTS.md` を読むことを明記。
- `employees/<department>/AGENTS.md`: 部署別の実務ルール。
- `employees/<department>/README.md`: 部署の説明。
- `employees/<department>/logs/`: 部署ごとの作業ログ保存先。作業ログは `YYYY-MM-DD.md` 形式で保存する。
- `employees/<department>/templates/`: 部署ごとの成果物テンプレート。

## 現在の部署

- 秘書: `employees/secretary/`
- リサーチ部: `employees/research/`
- クリエイティブ部: `employees/creative/`
- コミュニティ部: `employees/community/`
- マーケティング部: `employees/marketing/`
- プロダクト部: `employees/product/`

## 決定事項

- Codexで運用するため、`CLAUDE.md` は使わない。
- Codex向けの永続指示は `AGENTS.md` を使う。
- ただし、このプロジェクトでは `AGENT.md` を会社全体の共通ルールとして扱う。
- 部署作業の前に、必ずルートの `AGENT.md` を確認し、その後に該当部署の `employees/<department>/AGENTS.md` を読む。
- 投稿、DM、コメント、LINE配信、外部公開、販売実行はCodexが直接行わない。必ず人間承認後に実行する。
- すべての依頼はまず秘書を経由する。
- 秘書が内容を判断し、適切な部署に振り分ける。
- 部署を跨ぐ仕事は秘書が調整役を務める。
- 各部署の作業ログは部署ごとの `logs/YYYY-MM-DD.md` に保存する。
- 社長への報告は簡潔に行い、結論回避表現を避ける。
- 「やってみないとわかりません」「ケースバイケース」は禁止。
- 各部署はターゲット層（20代から40代の会社員、副業希望者）を踏まえた言葉選びをする。

## 部署別の主な設定

### 秘書

- 全依頼の受付、部署振り分け、部署間調整、承認待ち整理を担当。
- リサーチ、クリエイティブ、コミュニティ、マーケティング、プロダクトへの振り分け基準を `employees/secretary/AGENTS.md` に記載済み。

### リサーチ部

- インスタ運用に必要な情報源を握る。
- 競合アカウント分析は週2回。同ジャンル5アカウントを「テーマ・構成・ビジュアル・投稿時間」の4軸で分析。
- バズ投稿調査は毎日。5〜10件を収集し、なぜバズったかを一言で分析。
- トレンド調査は週1回。
- クリエイティブ部への引き継ぎ案を3つ提示する。

### クリエイティブ部

- インスタ投稿の全テキストを作る。
- フィード投稿は週3〜5本、10枚構成、1スライド最大40文字。
- 構成は「タイトル→共感→ノウハウ6枚→まとめ→CTA」。
- リール台本は週2〜3本。15秒、30秒、60秒のいずれか。
- ストーリーズ文言は毎日5〜8枚分。
- トーンは会話調、共感表現あり、煽り表現禁止。

### コミュニティ部

- アカウントの人間味を生む。
- 自分から送信するコメント案は1日15〜30件分。
- ターゲットはフォロワー500〜5,000人、同ジャンル、直近24時間以内に投稿があるアカウント。
- コメント文は60〜100文字。相手投稿に具体的に触れ、自分の経験を1〜2文添え、質問で終わる。
- 「素敵ですね！」だけの定型文、宣伝・URL付きコメント、初手の営業色は禁止。

### マーケティング部

- フォロワーをLINE読者に変える設計を担当。
- インスタ→LINE導線設計を行う。
- プロフィール導線、ストーリーズ導線、DM自動誘導、キャプションCTAを扱う。
- LINE配信シナリオは登録後7日間。
- ハッシュタグ戦略は大・中・小タグのミックス、月次見直し。
- `employees/marketing/AGENTS.md` のみLINE導線中心に更新済み。READMEやテンプレートは古い記述が残っている可能性がある。

### プロダクト部

- 販売商品の企画・制作を担当。
- フロントエンド、ミドル、バックエンドの商品ラインナップを定義済み。
- PDF教材、テンプレート集、LINE配信コンテンツ、Notion DB、インスタ運用マニュアル、講座カリキュラム、セミナー・ウェビナー台本を扱う。
- 企画プロセスは、悩みリサーチ、競合商品調査、差別化3点、商品概要書、制作、告知準備。

## 作成済みスキル

- Codex個人スキル: `C:\Users\yuuta\.codex\skills\weekly-post-ideas\`
- スキル名: `weekly-post-ideas`
- 用途: 毎週月曜朝に、来週分のInstagram投稿ネタ5案を作る。
- 保存先ルール:
  - 結果: `employees/creative/logs/YYYY-Www_next_week_ideas.md`
  - 秘書todo: `employees/secretary/todos/YYYY-MM-DD.md`
- 検証スクリプトはローカルPythonの `PyYAML` 不足で実行できなかったが、`SKILL.md` と `agents/openai.yaml` は作成済み。

## 未完了タスク

- 直近の変更をコミットし、GitHubへpushする。
- 必要であれば、マーケティング部の `README.md` とテンプレートもLINE導線中心の内容に揃える。
- `employees/secretary/todos/` フォルダを作るか決める。
- 週次投稿ネタ出しスキルを実際に走らせ、初回の `employees/creative/logs/YYYY-Www_next_week_ideas.md` を作る。
- 各部署の `logs/` に初回ログを作る運用を始める。
- `AGENT.md` と `AGENTS.md` の役割が重複しすぎていないか、今後必要に応じて整理する。

## 新しいスレッドで再開する時のおすすめ依頼文

```text
AGENT.md、AGENTS.md、CONTEXT.md を読んで、Instagram運用会社の続きから進めてください。まず現在の構成と未完了タスクを確認してください。
```


