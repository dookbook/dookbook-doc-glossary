# dookbook-doc-glossary

Dookbook&reg; (Developers' Cookbook) Document Library (Subject: **Glossary**)

开发者的日常菜谱 - 文档库**术语表**

## Getting Started 快速入门

Please refer to [about Dookbook&reg;](https://dookbook.info/about/)

请参考[关于Dookbook&reg;](https://dookbook.info/about/zh-hans/)

### Preparation in advance 前期准备

1. Clone this repo 克隆仓库
2. Open and install [GitHub App](https://github.com/apps/dookbook).
   打开并安装[GitHub App](https://github.com/apps/dookbook)
3. Add original (upstream) repo into your local git 增加上游仓库地址到你本地

```bash
git remote add upstream https://github.com/dookbook/dookbook-doc-glossary.git
```

### Synchronization with original (upstream) repo 与上游同步

```bash
git pull upstream master

git push origin master
```

### Attention 注意事项

- Submitting documents with topic branches is recommended 建议用主题分支提交文档

```bash
git checkout <topic-branch>
git pull
git rebase master
git push

<commits ...>

git push
```

- All documents in this library are written in **Markdown**,
more details please refer to [Dookbook Help - Markdown](https://dookbook.info/en/help/markdown/)
此文档库中所有的文档都是由**Markdown**语言撰写，所支持的语法规则及示例
请参考[Dookbook帮助 - Markdown](https://dookbook.info/zh-hans/help/markdown/)

- It's better to submit only minor changes at a time and write clear **Commit Messages**.
最好每次只提交较小的修改，并写好清晰明确的**Commit Messages（提交说明）**.
