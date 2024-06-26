# 前言

这本书是关于 Vue.js 的。我们将开始我们的旅程，试图理解 Vue.js 是什么，它与其他框架相比如何，以及它允许我们做什么。我们将在构建小型有趣的应用程序的同时学习 Vue.js 的不同方面，并将这些方面应用到实践中。最后，我们将回顾所学到的内容，并展望未来，看看我们还能学到什么并做些什么。因此，您将学到以下内容：

+   Vue.js 是什么以及它是如何工作的

+   Vue.js 的响应性和数据绑定

+   Vue.js 可重用组件

+   Vue.js 的插件

+   测试和部署使用 Vue.js 编写的应用程序

本书中的所有示例都是基于最近发布的 Vue 2.0 版本构建的。该书还包含了对先前版本的引用，涉及框架的已弃用或已更改的方面。

我相信您会喜欢使用本书构建 Vue.js 应用程序的过程。

# 本书涵盖的内容

第一章《使用 Vue.js 购物》，包括对 Vue.js 的介绍，本书中使用的术语以及第一个基本示例。

第二章《基础知识-安装和使用》解释了 Vue.js 的幕后情况，提供了对架构模式的理论见解，涵盖了几乎所有主要的 Vue.js 概念，并引导了本书中将开发的应用程序。

第三章《组件-理解和使用》深入探讨了组件，并解释了如何使用简单的组件系统和单文件组件重写应用程序。

第四章《响应性-将数据绑定到您的应用程序》详细解释了 Vue.js 中数据绑定机制的用法。

第五章《Vuex-管理应用程序中的状态》包含了对 Vuex 的详细介绍，Vuex 是 Vue.js 的状态管理系统，并解释了如何在应用程序中使用它以实现良好的可维护架构。

第六章，“插件-用自己的砖头建造你的房子”，展示了如何在 Vue 应用程序中使用插件，并解释了如何在应用程序中使用现有插件，并解释了如何构建我们自己的插件然后使用它。

第七章，“测试-测试我们到目前为止所做的事情的时间！”，包含了 Vue 应用程序中可以使用的测试技术的介绍，以将它们带到所需的质量水平。我们通过展示如何编写单元测试以及如何为本书中的应用程序开发端到端测试来解决这个问题。

第八章，“部署-是时候上线了！”，展示了如何将您的 Vue 应用程序带到世界上，并通过持续集成工具保证其质量。它解释了如何将 GitHub 存储库连接到 Travis 持续集成系统和 Heroku 云部署平台。

第九章，“接下来是什么”，总结了到目前为止所做的一切，并留给读者后续步骤。

附录，“练习解决方案”，提供了前三章练习的解决方案。

# 这本书需要什么

这本书的要求如下：

+   带有互联网连接的计算机

+   文本编辑器/集成开发环境

+   Node.js

# 这本书适合谁

这本书适用于 Web 开发人员或想要成为 Web 开发人员的人。无论您刚开始使用 Web 技术还是已经是 Web 技术浩瀚海洋中框架和语言的大师，这本书可能会在响应式 Web 应用程序的世界中向您展示一些新东西。如果您是 Vue 开发人员并且已经使用过 Vue 1.0，这本书可能是您迁移到 Vue 2.0 的有用指南，因为本书的所有示例都基于 Vue 2.0。即使您已经在使用 Vue 2.0，这本书也可能是一个很好的练习，从头开始构建一个应用程序，应用所有 Vue 和软件工程概念，并将其推向部署阶段。

至少需要一些技术背景。如果你已经能够用 JavaScript 编写代码，那将是一个巨大的优势。

# 惯例

在本书中，您将找到许多文本样式，用于区分不同类型的信息。以下是这些样式的一些示例以及它们的含义解释。

文本中的代码单词、数据库表名、文件夹名、文件名、文件扩展名、路径名、虚拟 URL、用户输入和 Twitter 用户名都会显示如下：“您的插件必须提供`install`方法。”

代码块设置如下：

```js
export default {
  components: {
    ShoppingListComponent,
    ShoppingListTitleComponent
  },
  computed: mapGetters({
    shoppinglists: 'getLists'
  })
}
```

当我们希望引起您对代码块的特定部分的注意时，相关行或项目将以粗体显示：

```js
export default {
  components: {
    ShoppingListComponent,
    ShoppingListTitleComponent
  },
  computed: mapGetters({
    shoppinglists: 'getLists'
  }),
  **methods: mapActions(['populateShoppingLists']),**
  store,
  **mounted () {**
**    this.populateShoppingLists()**
**  }**
}
```

任何命令行输入或输出都会按照以下方式书写：

```js
**cd shopping-list**
**npm install vue-resource --save-dev**

```

**新术语**和**重要单词**以粗体显示。您在屏幕上看到的单词，例如菜单或对话框中的单词，会以这种方式出现在文本中：“勾选**`开发者模式`**复选框”。

### 注意

警告或重要说明会出现在这样的框中。

### 提示

提示和技巧会以这种方式出现。
