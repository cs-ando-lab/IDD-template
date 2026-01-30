# 🚀 Issue Driven Development Starter Kit

> **Note**
> このリポジトリは「Issue駆動開発 (IDD)」を実践するためのテンプレートです。
> 右上の `Use this template` ボタンから新しいリポジトリを作成して利用してください。

## 📖 概要

「**No Issue, No Code**（Issueなくしてコードなし）」を原則とする開発テンプレートです。
個人開発からチーム開発まで、要件定義と実装の紐付けを強制し、開発迷子を防ぎます。

### 特徴
- 👮 **IDD Guard**: Issueと紐付かないPRをCIでブロック (.github/workflows/idd-guard.yml)
- 📝 **Smart Templates**: 用途に応じたIssue/PRテンプレート (Feature / Bug / Quick Task)
- 🏷 **Label as Code**: 設定ファイルベースのラベル自動同期 (.github/labels.yml)
- 🎨 **Standardized Labels**: 視認性の高いラベルセット定義済み

---

## 🛠 セットアップ (最初にやること)

リポジトリを作成したら、以下の手順で初期設定を行ってください。

### 1. ラベルの同期権限設定
`.github/workflows/label-sync.yml` がラベルを作成・削除できるように権限を設定します。

1. リポジトリの **Settings** > **Actions** > **General** を開く。
2. **Workflow permissions** 項目で **Read and write permissions** を選択する。
3. `Save` をクリック。
4. `.github/labels.yml` を少し編集してCommit（またはWorkflowを手動実行）すると、ラベルが自動反映されます。

### 2. プロジェクト情報の記述
テンプレートからリポジトリを作成したときに自動的に `README.md` が生成されます。
プロジェクトの概要、セットアップ方法、使い方などを記述してください。

---

## 🤝 開発ルール (Development Flow)

### 1. Issue First
コードを書く前に必ずIssueを作成します。

| テンプレート     | 用途                                                      |
| :--------------- | :-------------------------------------------------------- |
| **🚀 Feature**    | 新機能の実装。要件と完了条件(DoD)を明確にする場合に利用。 |
| **🐛 Bug Report** | バグ報告。再現手順と期待する動作を記述。                  |
| **⚡ Quick Task** | 個人の備忘録、雑務、リファクタリングなど。                |

### 2. Branch Naming
Issue番号を含めたブランチ名を作成します。

- `feature/{Issue番号}-{概要}` (例: `feature/10-login-screen`)
- `fix/{Issue番号}-{概要}` (例: `fix/12-submit-error`)
- `refactor/...`, `docs/...`

### 3. Pull Request
PRを作成する際は、テンプレートに従い `Closes #{Issue番号}` を必ず記述してください。
記述がない場合、**IDD Guard** によりマージがブロックされます。

---

## 🛡️ Pull Request の制約 (Constraints)

このリポジトリでは、開発プロセスと品質を維持するため、CI (GitHub Actions) によって以下のルールを強制しています。
ルールに違反している PR は**自動的にチェックが失敗し、マージできません。**

### 1. Issue との紐付け (必須)
PR の説明欄 (Body) に、必ず対応する Issue 番号への紐付けキーワードを記述してください。
「どの Issue に対する変更なのか」を明確にするためです。

- ✅ `Closes #10`
- ✅ `Fixes #25`
- ❌ (記述なし)

### 2. タイトルの命名規則 (Conventional Commits)
PR のタイトルは、変更内容が一目でわかるよう以下のフォーマットに従ってください。

**書式:** `Type: 概要`
**例:** `feat: ログイン機能の実装`

| Type | 説明 |
| :--- | :--- |
| `feat` | 新機能の追加 (Features) |
| `fix` | バグ修正 (Bug Fixes) |
| `docs` | ドキュメントのみの変更 |
| `style` | コードの動作に影響しない変更 (フォーマット, 空白など) |
| `refactor` | リファクタリング (機能追加やバグ修正を含まない) |
| `perf` | パフォーマンス改善 |
| `test` | テストの追加・修正 |
| `chore` | ビルドツールやライブラリの更新など |

### 3. テンプレートの記入
PR 作成時に自動挿入されるテンプレートのチェックリストは、すべて確認・記入してください。
特に「完了条件 (DoD)」は、Issue で定義された要件を満たしているかの重要な判定基準となります。

---

## 🏷 ラベル定義

| ラベル           | 色         | 説明           |
| :--------------- | :--------- | :------------- |
| `Type: Feature`  | 🔵 水色     | 新機能・改善   |
| `Type: Bug`      | 🔴 赤色     | 不具合・エラー |
| `Type: Task`     | ⚪ 灰色     | タスク・雑務   |
| `Priority: High` | 🟠 オレンジ | 優先度高       |
| `Status: WIP`    | 👚 薄赤     | 作業中         |
| `Status: Review` | 🧊 薄青     | レビュー待ち   |

---

## 📄 ライセンス

このリポジトリは [MIT License](LICENSE) の下でライセンスされています。