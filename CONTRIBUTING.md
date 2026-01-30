# Development Guide

このリポジトリは **Issue Driven Development (IDD)** で運用されています。

## 基本ルール
1. **No Issue, No Code**: コードを書く前に必ずIssueを立ててください。
2. **Task vs Feature**: 
    - しっかり設計する機能は `Feature` テンプレート
    - 細かい作業は `Quick Task` テンプレート
    - 使い分けてストレスなくIssue化しましょう。
3. **Pull Request**: PRを作成する際は、必ず対象のIssue番号を `Closes #xx` で紐付けてください。

## ブランチ命名規則
- `feature/issue番号-概要` (例: `feature/12-login`)
- `fix/issue番号-概要` (例: `fix/15-bug-fix`)