English | [中文](./README.zh-CN.md)

# git-commit-lint-vscode

In daily development, the mainstream code management tool is currently `git`. When we make changes to the code, we first need to `git commit` to submit it to the local repository. `git` requires that when submitting, we must fill in the submission information as a description of the changes, which will be saved in the `commit` history. This makes it possible to find historical code, facilitates review by others, and can also output a CHANGELOG, which greatly improves the development quality of the project.

However, in our usual work, most people simply fill in the `commit` without paying much attention to it, which is undoubtedly unfriendly to project management and maintenance. This plugin is used to standardize the `git` submission specifications, making your submission not only "good-looking" but also "practical."

## Where to start with standardizing `git` submissions?

Where does the standardization of `git` submissions begin? Where does it originate? Well, this can be traced back to `Angular`! Let's take a look at the submission specifications of the `Angular` community.
![](static/angular.png)

Isn't this commit record clear at a glance? Therefore, it is still necessary to follow the `git commit` specifications!

## explain

|   类型   | emji |           描述            |
| :------: | :--: | :-----------------------: |
|   feat   |  ✨  |        引入新功能         |
|   fix    |  🐛  |         修复 bug          |
|  style   |  💄  |    更新 UI 样式文按键     |
|  format  |  🥚  |        格式化代码         |
|   docs   |  📝  |       添加/更新文档       |
|   perf   |  👌  |       提高性能/优化       |
|   init   |  🎉  |    初次提交/初始化项目    |
|   test   |  ✅  |       增加测试代码        |
| refactor |  🎨  |   改进代码结构/代码格式   |
|  patch   |  🚑  |       添加重要补丁        |
|   file   |  📦  |        添加新文件         |
| publish  |  🚀  |        发布新版本         |
|   tag    |  📌  |        发布新版本         |
|  config  |  🔧  |       修改配置文件        |
|   git    |  🙈  | 添加或修改.gitignore 文件 |

## usage effect

![](static/git-commit-lint.png)

## instructions

- 1
  ![](static/first.png)
- 2
  ![](static/then.png)

## download

在 vscode 扩展中搜索 `git-commit-lint-vscode` 即可找到该插件。

## plug-in-configuration

![](static/extend.png)

你可以在 vscode 的 文件 -> 首选项 -> 设置 -> 扩展 -> git-commit-lint-vscode 中对该插件进行配置，目前可选的配置项为：

1. Accurate Locating: 当存在多个存储库时，是否精确定位到选定存储库的输入框，默认为`否`。注：该功能在多数情况下可以正常运行，只有当你的源代码管理存储库存在多个存储库，如只选择部分存储库或顺序错误时，就会选中错误的输入框。
2. Cover Input Value: 是否覆盖提交信息, 默认为`是`。如果取消勾选，则会在之前的提交信息前插入 emoji 或者 code。
3. Custom Format: 自定义 git 提交格式, 默认为`${emoji}${code}: `。可以完全自定义 参数取`Custom Type`里面的`key`
4. Custom Type: 自定义 git 提交类型, 默认为

```json
[
  {
    "emoji": "✨",
    "type": "feat",
    "name": "引入新功能",
    "description": "新功能"
  },
  {
    "emoji": "🐛",
    "type": "fix",
    "name": "修复bug",
    "description": "bug"
  },
  {
    "emoji": "💄",
    "type": "style",
    "name": "更新UI样式文件",
    "description": "样式"
  },
  {
    "emoji": "🥚",
    "type": "format",
    "name": "格式化代码",
    "description": "格式化"
  },
  {
    "emoji": "📝",
    "type": "docs",
    "name": "添加/更新文档",
    "description": "文档"
  },
  {
    "emoji": "👌",
    "type": "perf",
    "name": "提高性能/优化",
    "description": "优化"
  },
  {
    "emoji": "🎉",
    "type": "init",
    "name": "初次提交/初始化项目",
    "description": "初始化"
  },
  {
    "emoji": "✅",
    "type": "test",
    "name": "增加测试代码",
    "description": "测试"
  },
  {
    "emoji": "🎨",
    "type": "refactor",
    "name": "改进代码结构/代码格式",
    "description": "优化"
  },
  {
    "emoji": "🚑",
    "type": "patch",
    "name": "添加重要补丁",
    "description": "补丁"
  },
  {
    "emoji": "📦",
    "type": "file",
    "name": "添加新文件",
    "description": "新文件"
  },
  {
    "emoji": "🚀",
    "type": "publish",
    "name": "发布新版本",
    "description": "新版本"
  },
  {
    "emoji": "📌",
    "type": "tag",
    "name": "发布版本/添加标签",
    "description": "书签"
  },
  {
    "emoji": "🔧",
    "type": "config",
    "name": "修改配置文件",
    "description": "配置"
  },
  {
    "emoji": "🙈",
    "type": "git",
    "name": "添加或修改.gitignore文件",
    "description": "不可见"
  }
]
```

## participation contribution

Although it's just a small plugin, and maybe not many people use it, but thanks to all the contributors!

<a href="https://github.com/UvDream/git-commit-lint-vscode/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=UvDream/git-commit-lint-vscode" />
</a>

## issues

During use, you can ask questions here, and any requirements can also be raised here.

https://github.com/UvDream/git-commit-lint-vscode/issues
