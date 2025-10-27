# 概述

本指南旨在为习惯了形式化语言的程序员，以及所有追求精准、逻辑清晰的烹饪爱好者，提供一份详尽且易于理解的家庭烹饪手册。我们发现，网络上的许多菜谱描述随意、步骤模糊，常常导致操作者在实际烹饪过程中遇到困惑。为了解决这一问题，本项目致力于将烹饪过程标准化、结构化，确保任何人按照同一份菜谱操作，都能得到稳定且可预期的结果。

## 指南特色

- **精准量化**：我们摒弃“少许”、“适量”等模糊描述，尽可能对所有食材和调味料进行精确称量，并明确烹饪的时间和温度参数。
- **逻辑清晰**：每个菜谱都遵循严格的结构，包括原料清单、厨具需求、详细步骤和最终成品检验标准，使烹饪过程如同一段严谨的代码执行。
- **社区驱动**：这是一个开源项目，我们鼓励社区成员贡献新的菜谱、优化现有流程，共同维护这份知识库。所有内容都旨在方便二次开发和机器读取，使其成为未来智能化生命管理体系中的一个可靠模块。
- **非商业化**：本指南将永久保持非商业性质，不插入任何广告，不与特定品牌挂钩，专注于提供纯粹、可靠的烹饪知识。

## 指南结构

为了满足不同水平用户的需求，本指南内容被划分为几个核心模块。您可以根据自己的情况，选择从合适的章节开始。

```d2
direction: down

Cooking-Guide: "烹饪指南"

Cooking-Guide.Overview: "概述"

Cooking-Guide.Cooking-Basics: "烹饪入门" {
  Kitchen-Preparation: "厨房准备"
  Basic-Skills: "基础技巧"
  Common-Tools: "常用厨具"
}

Cooking-Guide.Recipe-Collection: "菜谱大全" {
  label: "菜谱大全 (核心部分)"
  style.fill: "#e6f7ff"
  
  Index-by-Difficulty: "按难度索引"
  Category-by-Ingredient: "按食材分类"
}

Cooking-Guide.Advanced-Knowledge: "进阶知识" {
  Advanced-Skills: "高级烹饪技巧"
  Theory: "理论知识"
}

Cooking-Guide -> Cooking-Guide.Overview
Cooking-Guide -> Cooking-Guide.Cooking-Basics
Cooking-Guide -> Cooking-Guide.Recipe-Collection
Cooking-Guide -> Cooking-Guide.Advanced-Knowledge

Cooking-Guide.Cooking-Basics -> Cooking-Guide.Cooking-Basics.Kitchen-Preparation
Cooking-Guide.Cooking-Basics -> Cooking-Guide.Cooking-Basics.Basic-Skills
Cooking-Guide.Cooking-Basics -> Cooking-Guide.Cooking-Basics.Common-Tools

Cooking-Guide.Recipe-Collection -> Cooking-Guide.Recipe-Collection.Index-by-Difficulty
Cooking-Guide.Recipe-Collection -> Cooking-Guide.Recipe-Collection.Category-by-Ingredient

Cooking-Guide.Advanced-Knowledge -> Cooking-Guide.Advanced-Knowledge.Advanced-Skills
Cooking-Guide.Advanced-Knowledge -> Cooking-Guide.Advanced-Knowledge.Theory

```

<x-cards data-columns="2">
  <x-card data-title="烹饪入门" data-icon="lucide:chef-hat" data-href="/basics">
    为烹饪新手准备的基础知识，涵盖厨房准备、基本刀工、火候控制，以及高压锅、空气炸锅等常用厨具的学习。
  </x-card>
  <x-card data-title="菜谱大全" data-icon="lucide:book-open-check" data-href="/recipes">
    本指南的核心，收录了大量经过验证的菜谱。您可以根据烹饪难度或主要食材进行浏览和检索。
  </x-card>
  <x-card data-title="进阶知识" data-icon="lucide:graduation-cap" data-href="/advanced">
    为有一定基础的用户提供，内容包括辅料技巧、高级烹饪术语、糖色炒制和油温判断等，帮助您的厨艺更上一层楼。
  </x-card>
  <x-card data-title="如何贡献" data-icon="lucide:github">
    我们欢迎您参与贡献！您可以直接修改发现的问题并提交 Pull request，或使用菜谱模板添加新的菜谱。
  </x-card>
</x-cards>

## 本地部署

如果您希望在本地环境中运行本菜谱的 Web 服务，可以按照以下步骤操作。请确保您的系统中已安装 Docker。

```bash Docker
# 拉取最新的 Docker 镜像
docker pull ghcr.io/anduin2017/how-to-cook:latest

# 在后台运行容器，并将服务的 80 端口映射到本地的 5000 端口
docker run -d -p 5000:80 ghcr.io/anduin2017/how-to-cook:latest
```

部署成功后，您可以通过浏览器访问 `http://localhost:5000` 来查看本地菜谱服务。