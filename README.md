# jihad

Tips to improve productivity and **DevEx**(Developer Experience)

## Best practice

| Link                                                                                                                                                                     | Description                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Conventional Commits](https://www.conventionalcommits.org/ja/v1.0.0/)                                                                                                   | Commit message specification such as<br>`docs: correct spelling of CHANGELOG`<br>`feat(api)!: send an email to the customer when a product is shipped` |
| [Semantic Versioning](https://semver.org/lang/ja/)                                                                                                                       | Resolve compatibility issues with `MAJOR.MINOR.PATCH` versioning (e.g., `1.12.358`).                                                                   |
| [Beyond the Twelve-Factor App](https://zenn.dev/kazurof/articles/18256f0e9c4761)                                                                                         | 15 practice for modern SaaS                                                                                                                            |
| [3factor app](https://3factor.app/)                                                                                                                                      | Impl of _Event Driven Architecture_ using **GraphQL**                                                                                                  |
| [Agile Software Development](https://www.sei-info.co.jp/framework/column/agile/)                                                                                         | Agile? Scrum? _Extreme Programming_?                                                                                                                   |
| [Four Keys](https://cloud.google.com/blog/ja/products/gcp/using-the-four-keys-to-measure-your-devops-performance) or [SPACE](https://note.com/dai___you/n/n117357da25b5) | Developer Productivity Framework                                                                                                                       |

## Tool

### Diagram

#### draw.io

Using `.[dio|drawio].[svg|png]` (e.g.,[assets/ide.drawio.svg](assets/ide.drawio.svg)), you can easily both **display** and **edit** the image as shown below.

[![Image link was broken!!!](assets/ide.drawio.svg)](https://app.diagrams.net/?url=https://raw.githubusercontent.com/mineco13/jihad/refs/heads/main/assets/ide.drawio.svg)

**Click** the image to edit online (not saved on GitHub), or use [IDEs](#ide) and more to edit locally :D

### Command Line Interface

**See [Taskfile.yaml](Taskfile.yaml)**

- OR use [VSCode Extension](https://taskfile.dev/integrations/)
  - OR install [Taskfile](https://taskfile.dev/), YAML based task runner / build tool alt to _makefile_, and run
    ```bash
    task -l
    ```

### Integrated Development Environment

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

### Browser extension

#### [Vimium](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=ja-jp)

<details><summary>Edit <b>Custom key mappings</b> on chrome-extension://dbepggeogbaibhgnhhndojpepiihcmeb/pages/options.html
</summary>

```conf
# Insert your preferred key mappings here.
map s scrollPageUp
map d scrollPageDown
unmap f # Disable Vimium's main feature
map <m-e> nextTab
map <m-d> openCopiedUrlInNewTab # Web search for text by 1.select the text, 2.`Command + c`, 3.`Command + d`.

# NOTICE for Linux or Windows users,
# REPLACE <m-*>, means `Command + *`, with <c-*>, means `Ctrl + *`.

```

</details>

### Personal Knowledge Management

| Name                                       | Killer feature                                                                                                                                                            |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Logseq](https://logseq.com/)              | [Link](https://docs.logseq.com/#/page/why%20linking%20matters), [Indentation](https://docs.logseq.com/#/page/what%20is%20indentation%20and%20why%20does%20it%20matter%3F) |
| [Notion](https://www.notion.so/ja/product) | [Database](https://www.notion.so/ja-jp/help/intro-to-databases)                                                                                                           |
