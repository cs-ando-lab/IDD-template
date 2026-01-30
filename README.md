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
この `README.md` の内容を、あなたのプロジェクトの内容に書き換えてください。
(以下の「開発ルール」セクションは、チームへの共有用として残しておくことを推奨します)

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