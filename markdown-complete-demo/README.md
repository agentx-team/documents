---
title: "markdown_complete_demo"
description: "Imported from documents/markdown_complete_demo.md"
tags: [md, imported]
icon: description
---

# Markdown 完整特性示例文档

> **文档说明：** 本文档基于《测试文档》编写，作者：**李南希**。  
> 本文件演示 Markdown 的所有主要特性，可作为语法参考手册使用。

---

## 目录

- [1. 标题（Headings）](#1-标题)
- [2. 段落与换行](#2-段落与换行)
- [3. 强调（Emphasis）](#3-强调)
- [4. 引用块（Blockquote）](#4-引用块)
- [5. 列表（Lists）](#5-列表)
- [6. 代码（Code）](#6-代码)
- [7. 水平分割线（Horizontal Rule）](#7-水平分割线)
- [8. 链接（Links）](#8-链接)
- [9. 图片（Images）](#9-图片)
- [10. 表格（Tables）](#10-表格)
- [11. 任务列表（Task List）](#11-任务列表)
- [12. 脚注（Footnotes）](#12-脚注)
- [13. 定义列表（Definition List）](#13-定义列表)
- [14. 删除线与下划线](#14-删除线与下划线)
- [15. 内联 HTML](#15-内联-html)
- [16. 转义字符](#16-转义字符)
- [17. Emoji](#17-emoji)
- [18. 数学公式（Math）](#18-数学公式)
- [19. 折叠块（Details/Summary）](#19-折叠块)
- [20. Front Matter（元数据）](#20-front-matter)

---

## 1. 标题

Markdown 支持六级标题，使用 `#` 号表示层级。

# 一级标题（H1）
## 二级标题（H2）
### 三级标题（H3）
#### 四级标题（H4）
##### 五级标题（H5）
###### 六级标题（H6）

也可以使用下划线语法（仅支持 H1 / H2）：

一级标题（下划线写法）
====================

二级标题（下划线写法）
--------------------

---

## 2. 段落与换行

这是第一段。段落之间需要留一个空行来分隔。

这是第二段。  
在行尾加两个空格，可以实现段落内换行（软换行）。

这是第三段，内容较长时会自动折行，不需要手动换行。Markdown 会将连续的文字视为同一段落，只有空行才会创建新段落。

---

## 3. 强调

| 写法 | 效果 |
|------|------|
| `**粗体**` | **粗体** |
| `__粗体__` | __粗体__ |
| `*斜体*` | *斜体* |
| `_斜体_` | _斜体_ |
| `***粗斜体***` | ***粗斜体*** |
| `~~删除线~~` | ~~删除线~~ |
| `` `行内代码` `` | `行内代码` |

示例句子：**李南希** 是《测试文档》的作者，她对 *Markdown* 语法有深入研究，并撰写了这份 ***完整指南***。

---

## 4. 引用块

使用 `>` 创建引用块，支持嵌套。

> 这是一段引用文字。
> 引用可以跨多行。

> **李南希** 说：
> > 好的文档胜过千行注释。
> >
> > —— 《测试文档》

> ##### 引用块中的标题
>
> 引用块内部同样支持其他 Markdown 语法，例如 **加粗**、*斜体*、`代码` 等。
>
> - 列表项一
> - 列表项二

---

## 5. 列表

### 5.1 无序列表

使用 `-`、`*` 或 `+` 创建无序列表：

- 苹果
- 香蕉
  - 大蕉
  - 小米蕉
    - 皇帝蕉
- 橙子

### 5.2 有序列表

1. 第一步：打开编辑器
2. 第二步：新建文件
3. 第三步：编写内容
   1. 添加标题
   2. 添加正文
4. 第四步：保存文件

### 5.3 混合嵌套列表

1. 前端技术
   - HTML
   - CSS
   - JavaScript
     1. ES6+
     2. TypeScript
2. 后端技术
   - Python
   - Go
   - Java

---

## 6. 代码

### 6.1 行内代码

使用反引号包裹行内代码：`print("Hello, 李南希!")`

### 6.2 代码块（无语言高亮）

```
这是一个普通代码块
不指定语言时不会高亮
```

### 6.3 代码块（指定语言）

**Python 示例：**

```python
# 测试文档示例代码
# 作者：李南希

def greet(name: str) -> str:
    """返回问候语"""
    return f"你好，{name}！欢迎阅读《测试文档》。"

class Document:
    def __init__(self, title: str, author: str):
        self.title = title
        self.author = author

    def __repr__(self):
        return f"Document(title='{self.title}', author='{self.author}')"

if __name__ == "__main__":
    doc = Document(title="测试文档", author="李南希")
    print(greet(doc.author))
    print(doc)
```

**JavaScript 示例：**

```javascript
// 测试文档 - JavaScript 示例
const document = {
  title: "测试文档",
  author: "李南希",
  features: ["标题", "列表", "代码块", "表格"],
};

const greet = (name) => `你好，${name}！`;

console.log(greet(document.author));
document.features.forEach((f, i) => console.log(`${i + 1}. ${f}`));
```

**Bash 示例：**

```bash
#!/bin/bash
# 创建测试文档

AUTHOR="李南希"
FILENAME="markdown_complete_demo.md"

echo "文档作者：${AUTHOR}"
echo "正在创建文件：${FILENAME}"
touch "${FILENAME}"
echo "创建完成！"
```

**JSON 示例：**

```json
{
  "title": "测试文档",
  "description": "这个是个测试文档，文档中包含一个姓名：李南希",
  "author": {
    "name": "李南希",
    "role": "文档工程师"
  },
  "tags": ["markdown", "文档", "示例"],
  "version": "1.0.0"
}
```

**YAML 示例：**

```yaml
---
title: 测试文档
description: 这个是个测试文档，文档中包含一个姓名：李南希
author:
  name: 李南希
  role: 文档工程师
tags:
  - markdown
  - 文档
  - 示例
version: "1.0.0"
```

**SQL 示例：**

```sql
-- 查询文档信息
SELECT
    d.id,
    d.title,
    a.name AS author,
    d.created_at
FROM documents d
JOIN authors a ON d.author_id = a.id
WHERE a.name = '李南希'
ORDER BY d.created_at DESC;
```

---

## 7. 水平分割线

三种写法均可生成水平分割线：

使用 `---`：

---

使用 `***`：

***

使用 `___`：

___

---

## 8. 链接

### 8.1 行内链接

[访问 GitHub](https://github.com)

[带 Title 的链接](https://github.com "GitHub 官网")

### 8.2 引用链接

这是一个[引用式链接][ref-link]，链接定义可以放在文档任意位置。

另一个[引用链接][1]示例。

[ref-link]: https://www.example.com "示例网站"
[1]: https://www.markdown.org "Markdown 官网"

### 8.3 自动链接

直接用尖括号包裹 URL 或邮件地址：

<https://www.example.com>

<linanxi@example.com>

### 8.4 锚点链接（页内跳转）

[跳回顶部目录](#目录)

---

## 9. 图片

### 9.1 行内图片

![Markdown Logo](https://markdown-here.com/img/icon256.png "Markdown Logo")

### 9.2 引用式图片

![示例图片][logo]

[logo]: https://via.placeholder.com/150 "占位图片"

### 9.3 带链接的图片

[![可点击的图片](https://via.placeholder.com/100 "点击访问")](https://www.example.com)

---

## 10. 表格

### 10.1 基本表格

| 姓名   | 角色         | 邮箱                  |
|--------|-------------|----------------------|
| 李南希 | 文档工程师   | linanxi@example.com  |
| 张三   | 后端开发     | zhangsan@example.com |
| 李四   | 前端开发     | lisi@example.com     |

### 10.2 对齐方式

| 左对齐        |   居中对齐    |        右对齐 |
|:------------- |:-------------:| -------------:|
| 内容左对齐    |   内容居中    |    内容右对齐 |
| `:-`          |    `:-:`      |          `-:` |
| 100           |      200      |           300 |

### 10.3 含 Markdown 语法的表格

| 特性       | 语法示例          | 渲染效果         |
|------------|-----------------|-----------------|
| 粗体       | `**文字**`       | **文字**         |
| 斜体       | `*文字*`         | *文字*           |
| 行内代码   | `` `code` ``    | `code`           |
| 删除线     | `~~文字~~`       | ~~文字~~         |
| 链接       | `[文字](url)`   | [文字](#)        |

---

## 11. 任务列表

- [x] 编写文档大纲
- [x] 完成标题章节
- [x] 完成列表章节
- [x] 完成代码章节
- [x] 完成表格章节
- [ ] 审阅文档内容
- [ ] 发布到知识库
- [ ] 通知李南希确认

---

## 12. 脚注

Markdown 是一种轻量级标记语言[^1]，由 John Gruber[^gruber] 于 2004 年创建。

本文档由 **李南希**[^author] 根据《测试文档》整理编写。

[^1]: Markdown 是一种可以使用普通文本编辑器编写的标记语言。
[^gruber]: John Gruber 是美国作家、博主，Markdown 语言的创始人。
[^author]: 李南希，文档工程师，专注于技术写作与知识管理。

---

## 13. 定义列表

Markdown
:   一种轻量级标记语言，使用纯文本格式编写，可转换为 HTML 等格式。

Front Matter
:   文档头部的元数据块，通常使用 YAML 或 TOML 格式书写。
:   例如 `title`、`date`、`author` 等字段。

李南希
:   《测试文档》的作者，本示例文档的创建者。

---

## 14. 删除线与下划线

~~这段文字已被删除~~，请参考最新版本。

原作者：~~张三~~ → **李南希**（已更新）

> **注意：** 标准 Markdown 不支持原生下划线，部分扩展语法支持 `<u>下划线</u>` 写法：<u>下划线文字</u>

---

## 15. 内联 HTML

Markdown 支持直接嵌入 HTML 标签。

<div align="center">
  <h3>🎉 居中标题（HTML 实现）</h3>
  <p>作者：<strong>李南希</strong> | 文档版本：<code>v1.0.0</code></p>
</div>

<details>
  <summary>点击展开 HTML 表格示例</summary>
  <table>
    <tr>
      <th>字段</th>
      <th>值</th>
    </tr>
    <tr>
      <td>文档名称</td>
      <td>测试文档</td>
    </tr>
    <tr>
      <td>作者</td>
      <td>李南希</td>
    </tr>
  </table>
</details>

<br>

使用 `<br>` 可以强制换行，`<hr>` 也可以生成分割线：

<hr>

---

## 16. 转义字符

使用反斜杠 `\` 转义 Markdown 特殊字符：

| 原字符 | 转义写法 | 显示效果 |
|--------|---------|---------|
| `*`    | `\*`    | \*      |
| `_`    | `\_`    | \_      |
| `` ` ``| `` \` ``| \`      |
| `#`    | `\#`    | \#      |
| `[`    | `\[`    | \[      |
| `]`    | `\]`    | \]      |
| `(`    | `\(`    | \(      |
| `)`    | `\)`    | \)      |
| `>`    | `\>`    | \>      |
| `\`    | `\\`    | \\      |
| `!`    | `\!`    | \!      |
| `&`    | `\&`    | \&      |

---

## 17. Emoji

Markdown（部分渲染器）支持 Emoji 表情：

- 使用短代码：`:smile:` → 😄
- 直接粘贴：🚀 📄 ✅ ❌ ⚠️ 💡 🔥 🎯 📊 🛠️

文档状态：✅ 已完成 | 📝 编写中 | 🔍 审阅中 | 🚀 已发布

---

## 18. 数学公式

部分 Markdown 渲染器（如 MathJax、KaTeX）支持 LaTeX 数学公式。

### 18.1 行内公式

爱因斯坦质能方程：$E = mc^2$

二次方程求根公式：$x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}$

### 18.2 块级公式

$$
\int_{-\infty}^{+\infty} e^{-x^2} \, dx = \sqrt{\pi}
$$

$$
\begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

---

## 19. 折叠块

使用 HTML `<details>` 和 `<summary>` 标签实现可折叠内容：

<details>
<summary>📖 点击查看：文档元数据</summary>

```yaml
title: 测试文档
description: 这个是个测试文档，文档中包含一个姓名：李南希
author: 李南希
date: 2024-01-01
tags:
  - markdown
  - demo
  - 完整示例
```

</details>

<details>
<summary>🔧 点击查看：完整代码示例</summary>

```python
# 完整的文档处理示例
from dataclasses import dataclass
from typing import List

@dataclass
class Author:
    name: str
    email: str

@dataclass
class TestDocument:
    title: str
    description: str
    author: Author
    tags: List[str]

# 创建《测试文档》实例
doc = TestDocument(
    title="测试文档",
    description="这个是个测试文档，文档中包含一个姓名：李南希",
    author=Author(name="李南希", email="linanxi@example.com"),
    tags=["markdown", "demo", "完整示例"]
)

print(f"标题：{doc.title}")
print(f"作者：{doc.author.name}")
```

</details>

<details>
<summary>📋 点击查看：Markdown 语法速查</summary>

| 语法 | 功能 |
|------|------|
| `# 文字` | 一级标题 |
| `**文字**` | 粗体 |
| `*文字*` | 斜体 |
| `[文字](url)` | 链接 |
| `![描述](url)` | 图片 |
| `` `code` `` | 行内代码 |
| `> 文字` | 引用块 |
| `---` | 分割线 |
| `- [ ]` | 待办事项 |
| `- [x]` | 已完成事项 |

</details>

---

## 20. Front Matter

Front Matter 是文档头部的元数据块，使用 `---` 包裹，通常为 YAML 格式。  
本文档如果带有 Front Matter，其内容示例如下：

```yaml
---
title: "Markdown 完整特性示例文档"
description: "本文档基于《测试文档》编写，演示 Markdown 的所有主要特性"
author: "李南希"
date: "2024-01-01"
version: "1.0.0"
tags:
  - markdown
  - 语法
  - 示例
  - 完整文档
draft: false
toc: true
---
```

---

## 附录：Markdown 特性速览

| 特性分类       | 特性名称         | 标准支持 | 扩展支持 |
|:-------------|:---------------|:-------:|:-------:|
| 文本格式       | 标题（H1-H6）   | ✅      | ✅      |
| 文本格式       | 粗体            | ✅      | ✅      |
| 文本格式       | 斜体            | ✅      | ✅      |
| 文本格式       | 粗斜体          | ✅      | ✅      |
| 文本格式       | 删除线          | ❌      | ✅      |
| 结构元素       | 引用块          | ✅      | ✅      |
| 结构元素       | 无序列表        | ✅      | ✅      |
| 结构元素       | 有序列表        | ✅      | ✅      |
| 结构元素       | 任务列表        | ❌      | ✅      |
| 结构元素       | 水平分割线      | ✅      | ✅      |
| 代码           | 行内代码        | ✅      | ✅      |
| 代码           | 代码块          | ✅      | ✅      |
| 代码           | 语法高亮        | ❌      | ✅      |
| 富媒体         | 链接            | ✅      | ✅      |
| 富媒体         | 图片            | ✅      | ✅      |
| 富媒体         | 表格            | ❌      | ✅      |
| 扩展特性       | 脚注            | ❌      | ✅      |
| 扩展特性       | 定义列表        | ❌      | ✅      |
| 扩展特性       | 数学公式        | ❌      | ✅      |
| 扩展特性       | Emoji          | ❌      | ✅      |
| 扩展特性       | Front Matter   | ❌      | ✅      |
| 内联 HTML      | HTML 标签       | ✅      | ✅      |

---

<div align="center">

📄 **文档结束**

本文档由 **李南希** 根据《测试文档》整理编写  
涵盖 Markdown 标准规范及 GFM（GitHub Flavored Markdown）扩展特性

*如有问题，欢迎反馈与指正。*

</div>
