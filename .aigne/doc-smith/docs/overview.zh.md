# 概述

欢迎使用《程序员做饭指南》。本指南的创立源于一个简单的目标：用编写代码的严谨思维来呈现菜谱。许多在线菜谱描述模糊、步骤随意，对于习惯了精确与逻辑的程序员而言，这样的内容往往难以遵循。

因此，我们创建了这个项目，旨在提供一系列清晰、标准化且易于复现的烹饪说明，让任何人在家都能轻松、自信地做出美味佳肴。

## 核心理念

本指南不仅仅是一本菜谱的集合，它遵循着一套严谨的原则，以确保内容的准确性和实用性。

<x-cards data-columns="3">
  <x-card data-title="精确与标准化" data-icon="lucide:ruler">
    我们的菜谱力求形式化，避免使用“少许”、“适量”等模糊词汇。目标是让不同的烹饪者按照同一份菜谱，能做出味道和外观都高度一致的成品。这不仅方便人类阅读，也为机器处理和 AI 学习奠定了基础。
  </x-card>
  <x-card data-title="开源与社区驱动" data-icon="lucide:users">
    这是一个由社区共同维护的开源项目。我们欢迎任何人贡献新的菜谱、修正现有问题或提出改进建议。您的每一次参与都能让这个指南变得更加完善。
  </x-card>
  <x-card data-title="非商业与 AI 友好" data-icon="lucide:cpu">
    本指南将永久保持非商业化，不含广告，不为特定品牌背书。我们鼓励社区利用这些标准化的菜谱数据进行二次开发，例如训练烹饪 AI 或集成到健康管理应用中。
  </x-card>
</x-cards>

## 指南结构

为了方便您快速查找所需信息，我们将内容划分为以下几个核心部分：

```d2
direction: down

guide: {
  label: "程序员做饭指南"
  shape: rectangle
}

sections: {
  label: ""
  shape: rectangle
  style.stroke-width: 0

  basics: {
    label: "烹饪入门"
    tooltip: "厨房准备、基础技巧和常用厨具"
  }
  recipes: {
    label: "菜谱大全"
    tooltip: "所有菜谱的集合"
  }
  advanced: {
    label: "进阶知识"
    tooltip: "高级烹饪技巧和理论"
  }
}

recipes_sub: {
  label: ""
  shape: rectangle
  style.stroke-width: 0
  
  by_category: {
    label: "按食材分类"
  }
  by_difficulty: {
    label: "按难度索引"
  }
}

guide -> sections.basics: "新手"
guide -> sections.recipes: "核心"
guide -> sections.advanced: "高手"

sections.recipes -> recipes_sub.by_category
sections.recipes -> recipes_sub.by_difficulty
```

<x-cards>
  <x-card data-title="烹饪入门" data-icon="lucide:graduation-cap" data-href="/basics">
    为烹饪新手准备，涵盖厨房准备、基础技巧和常用厨具等知识，帮助您顺利开启烹饪之旅。
  </x-card>
  <x-card data-title="菜谱大全" data-icon="lucide:book-open" data-href="/recipes">
    收录了所有菜谱，您可以按照食材分类或烹饪难度进行浏览，快速找到心仪的菜肴。
  </x-card>
  <x-card data-title="进阶知识" data-icon="lucide:bar-chart-2" data-href="/advanced">
    专为有一定基础的烹饪爱好者设计，提供更高级的烹饪理论和技巧，助您厨艺更上一层楼。
  </x-card>
</x-cards>

## 如何贡献

本指南是一个开放的项目，我们鼓励您参与贡献。如果您发现了任何问题，或者想要添加一道拿手好菜，可以直接在我们的 GitHub 仓库中提交 Pull Request。我们提供了详细的菜谱模板以方便您撰写。

我们希望这份结构清晰、内容精准的烹饪指南能成为您厨房中的得力助手。现在，您可以从 [烹饪入门](./basics.md) 开始，或直接进入 [菜谱大全](./recipes.md) 探索美食。