# Reader Side

[English](README.md)

Reader Side は、作り手の作業過程を語るのではなく、実際の読み手の側から文章を書くための、移植可能な Agent Skill です。

PR本文、UI文言、issue、リリースノート、文書、報告、メールに何を書くべきかを、読み手が理解・判断・行動するために必要かどうかで決めます。

## 防ぐこと

- ローカルな指示や設定を、外部に残る成果物へ混ぜること。
- 実装途中の一時的な失敗や作業の時系列を、最終結果の説明として載せること。
- 利用者に必要な情報ではなく、内部の実装詳細をUI上で説明してしまうこと。
- 必要な情報が異なる利用者、レビュアー、保守担当者へ同じ説明を使い回すこと。
- スキルに従ったというメタ説明を完成した文章へ加えること。

Reader Side は短文化の規則でも、技術詳細を禁止する規則でもありません。未解決の失敗、リスク、制約、不確実性、移行要件、読み手に必要な根拠は残します。

## インストール

### Claude Code

次の2つを別々のプロンプトとして実行してください。

```text
/plugin marketplace add cannorin/reader-side
```

```text
/plugin install reader-side@reader-side
```

### Codex

シェルで次の2コマンドを実行してください。

```sh
codex plugin marketplace add cannorin/reader-side
codex plugin add reader-side@reader-side
```

インストール後、新しいセッションを開始してください。Claude Codeでは`/reader-side:reader-side`、Codexでは`$reader-side:reader-side`として明示的に呼び出せます。関連する依頼では自動的にも選択されます。

### その他のコーディングエージェント

`skills/reader-side/`を、次の個人用またはプロジェクト用ディレクトリへコピーしてください。

| エージェント | 個人用 | プロジェクト用 |
| --- | --- | --- |
| [Cursor](https://cursor.com/help/customization/skills) | `~/.cursor/skills/reader-side/` または `~/.agents/skills/reader-side/` | `.cursor/skills/reader-side/` または `.agents/skills/reader-side/` |
| [GitHub Copilot](https://docs.github.com/en/copilot/concepts/customizations/agent-skills) | `~/.copilot/skills/reader-side/` または `~/.agents/skills/reader-side/` | `.github/skills/reader-side/` または `.agents/skills/reader-side/` |
| [Gemini CLI](https://geminicli.com/docs/cli/tutorials/skills-getting-started/) | `~/.gemini/skills/reader-side/` | `.gemini/skills/reader-side/` または `.agents/skills/reader-side/` |

明示的に指定する場合は、次のように依頼します。

> reader-side を使って、このPR本文にレビュアーが必要としない情報が含まれていないか確認してください。
