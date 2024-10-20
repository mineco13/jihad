# method

Tips to improve productivity and DevEx(Developer Experience)

## Best practice

| Link                                                                                                                                                                     | Description                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------- |
| [Conventional Commits](https://www.conventionalcommits.org/ja/v1.0.0/)                                                                                                   | Commit message specification     |
| [Semantic Versioning](https://semver.org/lang/ja/)                                                                                                                       | Resolve dependency hell          |
| [The Twelve-Factor App](https://12factor.net/ja/)                                                                                                                        | Modern SaaS practice             |
| [3factor app](https://3factor.app/)                                                                                                                                      | Impl of EDA                      |
| [Agile Software Development](https://www.sei-info.co.jp/framework/column/agile/)                                                                                         | List of agile dev methods        |
| [Four Keys](https://cloud.google.com/blog/ja/products/gcp/using-the-four-keys-to-measure-your-devops-performance) or [SPACE](https://note.com/dai___you/n/n117357da25b5) | Developer Productivity Framework |

## Tool

### CLI

**See [Taskfile.yaml](Taskfile.yaml)**

- OR use [VSCode Extension](https://taskfile.dev/integrations/)
  - OR install [Taskfile](https://taskfile.dev/), YAML based task runner / build tool alt to `makefile`, and run
    ```bash
    task -l
    ```

### IDE

[JetBrains IDEs](https://www.jetbrains.com/ja-jp/ides/) are mentors that help me write quality code productively.(I switched from _Eclipse_.)\
[VSCode](https://code.visualstudio.com/) is a useful tool when combining multiple less mature technologies.

| Settings and Tips                                                                                          | JetBrains IDEs                                                                                                                                                                | VSCode                                                                                                        |
| ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Sync keymap by                                                                                             | [Install VSCode Keymap](https://plugins.jetbrains.com/plugin/12062-vscode-keymap) and [Apply it](https://pleiades.io/help/idea/configuring-keyboard-and-mouse-shortcuts.html) | -                                                                                                             |
| Assign `Ctrl + d` to                                                                                       | Search with Google                                                                                                                                                            | [extension.googleSearch](https://marketplace.visualstudio.com/items?itemName=kameshkotwani.google-search)     |
| [![Image link was broken!!!](assets/ide.drawio.svg)](assets/ide.drawio.svg)<br> Create and Edit diagram by | [`.drawio.svg` or `.drawio.png`](https://plugins.jetbrains.com/plugin/15635-diagrams-net-integration)                                                                         | [`.drawio.svg` or `.drawio.png`](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)    |
| Visualize Git by                                                                                           | Built-in windows [Commits](https://pleiades.io/help/idea/commit-and-push-changes.html#commit) and [Branches](https://pleiades.io/help/idea/manage-branches.html)              | [Extention](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)                           |
| Use `Ctrl + .` for                                                                                         | [Quick-fix](https://pleiades.io/help/idea/resolving-problems.html)                                                                                                            | [Quick-fix](https://code.visualstudio.com/docs/editor/refactoring#_code-actions-quick-fixes-and-refactorings) |
| Clean up code on commit by                                                                                 | [Built-in feature](https://pleiades.io/help/idea/running-inspections.html#run-before-commit)                                                                                  | ?                                                                                                             |

I love live coding assistance, such as
[spell checking](https://pleiades.io/help/idea/spellchecking.html),
[type matching completion](https://pleiades.io/help/idea/auto-completing-code.html#smart_type_matching_completion),
and [code analysis](https://pleiades.io/help/idea/file-and-project-analysis.html#analysis-current-file)
compromising performance.\
Free JetBrains IDEs are [IntelliJ IDEA](https://www.jetbrains.com/ja-jp/idea/) for [Java](https://ja.quarkus.io/) and [Kotlin](https://kotlinlang.org/docs/kotlin-tour-hello-world.html),
[RustRover](https://www.jetbrains.com/ja-jp/rust/) for [Rust](https://tourofrust.com/00_ja.html),
[PyCharm](https://www.jetbrains.com/ja-jp/pycharm/) for [Python](https://hub.docker.com/_/python),
and [JetBrains Fleet](https://www.jetbrains.com/ja-jp/fleet/#polyglot) for Multiple lang.(The Community editions and more are available.)

### Browser extension

#### [Vimium](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=ja-jp)

Edit **Custom key mappings** on chrome-extension://dbepggeogbaibhgnhhndojpepiihcmeb/pages/options.html

```conf
# Insert your preferred key mappings here.
map s scrollPageUp
map d scrollPageDown
unmap f # Disable Vimium's main feature
map <m-e> nextTab
map <m-d> openCopiedUrlInNewTab # Search for text by 1.select the text, 2.`Command + c`, 3.`Command + d`.

# NOTICE for Linux or Windows users,
# REPLACE <m-*>, means `Command + *`, with <c-*>, means `Ctrl + *`.

```

### PKM = Personal Knowledge Management tool

| Name                                       | Killer feature                                                                                                                                                            |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Logseq](https://logseq.com/)              | [Link](https://docs.logseq.com/#/page/why%20linking%20matters), [Indentation](https://docs.logseq.com/#/page/what%20is%20indentation%20and%20why%20does%20it%20matter%3F) |
| [Notion](https://www.notion.so/ja/product) | [Database](https://www.notion.so/ja-jp/help/intro-to-databases)                                                                                                           |
