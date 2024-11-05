# jihad

Tips to improve productivity and **DevEx**(Developer Experience)

## Best practice

| Link                                                                                                                                                                     | Description                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Conventional Commits](https://www.conventionalcommits.org/ja/v1.0.0/)                                                                                                   | Commit message specification.<br>ex.1: `docs: correct spelling of CHANGELOG`<br>ex.2: `feat(api)!: send an email to the customer when a product is shipped`             |
| [Conventional Comments](https://conventionalcomments.org/)                                                                                                               | Reduce communication costs between reviewers and coders.<br>See also [Google's Code Review Guidelines](https://fujiharuka.github.io/google-eng-practices-ja/ja/review/) |
| [Semantic Versioning](https://semver.org/lang/ja/)                                                                                                                       | Resolve compatibility issues with `MAJOR.MINOR.PATCH` versioning.<br>e.g., `1.12.358`                                                                                   |
| [Beyond the Twelve-Factor App](https://zenn.dev/kazurof/articles/18256f0e9c4761)                                                                                         | 15 Practices for Modern SaaS: Updating the Twelve-Factor App with 3 Additional Practices                                                                                |
| [3factor app](https://3factor.app/)                                                                                                                                      | Impl of _Event Driven Architecture_ using **GraphQL**                                                                                                                   |
| [Agile Software Development](https://www.sei-info.co.jp/framework/column/agile/)                                                                                         | Agile? Scrum? _Extreme Programming_?                                                                                                                                    |
| [Four Keys](https://cloud.google.com/blog/ja/products/gcp/using-the-four-keys-to-measure-your-devops-performance) or [SPACE](https://note.com/dai___you/n/n117357da25b5) | Developer Productivity Framework                                                                                                                                        |

## Tool

### [draw.io](https://www.drawio.com/) - Platform for Diagrams to Display & Edit

Using `.[dio|drawio].[svg|png]` (e.g.,[assets/ide.drawio.svg](assets/ide.drawio.svg)), you can easily both **display** and **edit** the image as shown below.

[![Image link was broken!!!](assets/ide.drawio.svg)](https://app.diagrams.net/?url=https://raw.githubusercontent.com/mineco13/jihad/refs/heads/main/assets/ide.drawio.svg)

**Click** the image to edit online (not saved on GitHub), or use [IDEs](#integrated-development-environment) and more to edit locally :D

### [Vimium](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=ja-jp) - Browser extension for Quick web search

<details><summary>Settings</summary>

Using the browser's address bar, access  
`chrome-extension://dbepggeogbaibhgnhhndojpepiihcmeb/pages/options.html`  
AND edit **Custom key mappings** as shown.

```conf
# Insert your preferred key mappings here.
map s scrollPageUp
map d scrollPageDown
unmap f # Disable Vimium's main feature
map <m-e> nextTab

map <m-d> openCopiedUrlInNewTab
# Web search for the text on the page
# 1. Select the text by double-clicking
# 2. `Command + c`
# 3. `Command + d`

# NOTICE for Linux or Windows users,
# REPLACE <m-*>, =`Command + *`, with <c-*>, =`Ctrl + *`.
```

</details>

### [Logseq](https://logseq.com/) - Connecting the Dots

<details><summary>Try it on the demo page. </summary>

Access https://demo.logseq.com/

1. Input your favorite text, press `Enter`, and it will create a **Block**.
2. Copy & Paste the following text, press `Enter`, and it will create a **Page**.

   ```md
   [[Logseq]]
   ```

3. Click on `[[Logseq]]`, then C&P the following text.

   ```md
   [[Block]] is atomic element of [[Logseq]]

   [[Page]] is array of [[Block]]

   [[Link]] shows how the current [[Page]] is referred to by other [[Page]]s.

         - [[Link]] also works similarly for [[Block]].
   ```

4. Click on `[[Link]]`, then C&P the following text.

   ```md
   `[[page]]`で page という題名の [[Page]] を検索し、選択することでその [[Page]] への `Link` を作成できる

         - 該当する [[Page]] が存在しない場合は自動で作成される

   `((block))`で block という文字列を含んだ [[Block]] を検索し、選択することでその[[Block]]への`Link`を作成できる
   ```

5. Click on [`Graph view`](https://demo.logseq.com/#/graph) and play

</details>

### CLI Tools - Essentials for Automation

Install Docker for [Linux](https://docs.docker.com/engine/install/) or [Mac](https://orbstack.dev/), [Windows](https://docs.docker.com/desktop/install/windows-install/).

**See [Taskfile.yaml](Taskfile.yaml)**

- OR install [Taskfile](https://taskfile.dev/), YAML based task runner / build tool alt to _makefile_, and
  - ```bash
    task -l
    ```
  - OR use [VSCode Extension](https://taskfile.dev/integrations/)

### JetBrains IDEs & VSCode - Essentials for Dev

[JetBrains IDEs](https://www.jetbrains.com/ja-jp/ides/) are mentors that help me write **quality** code **productively**.(I switched from _Eclipse_.)\
[VSCode](https://code.visualstudio.com/) is a useful tool when combining multiple less mature technologies.

<details><summary>Settings and Tips</summary>

|                                                | JetBrains IDEs                                                                                                                                                                | VSCode                                                                                                        |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Sync keymap by                                 | [Install VSCode Keymap](https://plugins.jetbrains.com/plugin/12062-vscode-keymap) and [Apply it](https://pleiades.io/help/idea/configuring-keyboard-and-mouse-shortcuts.html) | -                                                                                                             |
| Assign `Ctrl + d` to                           | [`Search with Google`](https://pleiades.io/help/idea/configuring-keyboard-and-mouse-shortcuts.html#add-keyboard-shortcut)                                                     | [`extension.googleSearch`](https://marketplace.visualstudio.com/items?itemName=kameshkotwani.google-search)   |
| Edit [`.[dio\|drawio].[svg\|png]`](#drawio) by | [Extension](https://plugins.jetbrains.com/plugin/15635-diagrams-net-integration)                                                                                              | [Extension](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)                         |
| Visualize Git by                               | Built-in windows [Commits](https://pleiades.io/help/idea/commit-and-push-changes.html#commit) and [Branches](https://pleiades.io/help/idea/manage-branches.html)              | [Extension](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)                           |
| Use `Ctrl + .` for                             | [Quick-fix](https://pleiades.io/help/idea/resolving-problems.html)                                                                                                            | [Quick-fix](https://code.visualstudio.com/docs/editor/refactoring#_code-actions-quick-fixes-and-refactorings) |
| Clean up code on commit by                     | [Built-in feature](https://pleiades.io/help/idea/running-inspections.html#run-before-commit)                                                                                  | ?                                                                                                             |

</details>

<details><summary><b>Free</b> JetBrains IDEs are <b>available</b> in Community editions and more.</summary>

| [IntelliJ IDEA](https://www.jetbrains.com/ja-jp/idea/)                                                                                           | [PyCharm](https://www.jetbrains.com/ja-jp/pycharm/) | [WebStorm](https://www.jetbrains.com/ja-jp/webstorm/) | [RustRover](https://www.jetbrains.com/ja-jp/rust/) | [Rider](https://www.jetbrains.com/ja-jp/rider/) | [JetBrains Fleet](https://www.jetbrains.com/ja-jp/fleet/#polyglot) |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------- | ----------------------------------------------------- | -------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------ |
| [Java](https://www.jetbrains.com/ja-jp/lp/devecosystem-2023/java/#java_ide) & [Kotlin](https://kotlinlang.org/docs/kotlin-tour-hello-world.html) | [Python](https://hub.docker.com/_/python)           | [TypeScript](https://www.typescriptlang.org/) & JS    | [Rust](https://tourofrust.com/00_ja.html)          | C#, F#, VB.NET                                  | Multiple lang                                                      |

I love **live coding assistance**, such as
[spell checking](https://pleiades.io/help/idea/spellchecking.html),
[type matching completion](https://pleiades.io/help/idea/auto-completing-code.html#smart_type_matching_completion),
and [code analysis](https://pleiades.io/help/idea/file-and-project-analysis.html#analysis-current-file).

</details>

### [Coda](https://coda.io/gallery/engineering) / [Notion](https://www.notion.so/ja/help/intro-to-databases) - Unified Database & Docs
