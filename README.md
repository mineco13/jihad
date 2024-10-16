# method

## Best practice

| Link                                                                             | Description                  |
| -------------------------------------------------------------------------------- | ---------------------------- |
| [Conventional Commits](https://www.conventionalcommits.org/ja/v1.0.0/)           | Commit message specification |
| [Semantic Versioning](https://semver.org/lang/ja/)                               | Resolve dependency hell      |
| [The Twelve-Factor App](https://12factor.net/ja/)                                | Modern SaaS practice         |
| [3factor app](https://3factor.app/)                                              | Impl of EDA                  |
| [Agile Software Development](https://www.sei-info.co.jp/framework/column/agile/) | List of agile dev methods    |
|                                                                                  |                              |

## Tool

### IDE

Using [Jetbrains products](https://www.jetbrains.com/ja-jp/ides/) for productiity and DX(Developer Experience)

| Keybind     |                                                                           |
| ----------- | ------------------------------------------------------------------------- |
| All         | [VSCode Keymap](https://plugins.jetbrains.com/plugin/12062-vscode-keymap) |
| Command + D | Search with Google                                                        |

| Name                                                               | Lang                                                                                               |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| [IntelliJ IDEA](https://www.jetbrains.com/ja-jp/idea/)             | [Java](https://ja.quarkus.io/), [Kotlin](https://kotlinlang.org/docs/kotlin-tour-hello-world.html) |
| [RustRover](https://www.jetbrains.com/ja-jp/rust/)                 | [Rust](https://tourofrust.com/00_ja.html)                                                          |
| [PyCharm](https://www.jetbrains.com/ja-jp/pycharm/)                | [Python](https://hub.docker.com/_/python)                                                          |
| [JetBrains Fleet](https://www.jetbrains.com/ja-jp/fleet/#polyglot) | Multiple                                                                                           |

### Browser extension

#### [Vimium](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=ja-jp)

Edit **Custom key mappings** on chrome-extension://dbepggeogbaibhgnhhndojpepiihcmeb/pages/options.html

```
# Insert your preferred key mappings here.
map <m-d> openCopiedUrlInNewTab
map <m-e> nextTab
map s scrollPageUp
map d scrollPageDown
unmap f
```

Except Mac, replace `<m-X>` by `<c-X>`

### PKM = Personal Knowledge Management tool

| Name                                       | Killer feature                                                                                                                                                            |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Logseq](https://logseq.com/)              | [Link](https://docs.logseq.com/#/page/why%20linking%20matters), [Indentation](https://docs.logseq.com/#/page/what%20is%20indentation%20and%20why%20does%20it%20matter%3F) |
| [Notion](https://www.notion.so/ja/product) | [Database](https://www.notion.so/ja-jp/help/intro-to-databases)                                                                                                           |

## multipass

```sh
export VM_NAME=knative && multipass delete --purge $VM_NAME && multipass launch --name $VM_NAME --cloud-init multipass.yaml --cpus 6 --memory 12G --disk 40G docker && multipass exec $VM_NAME -- ls .ssh
```

```sh
ssh  -i ~/.ssh/id_rsa ubuntu@$(multipass exec knative -- ip -br -4 a|grep enp0s1|awk '{print $3}'|sed 's/\/[0-9]*$//')
```

```sh
multipass restart knative
```
