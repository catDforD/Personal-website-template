# Markdown 语法示例 / Markdown Syntax Example

这是一篇展示 Markdown 各种语法用法的示例文章。/ This is an example article showing Markdown syntax.

## 标题 / Headings

Markdown 支持六级标题：/ Markdown supports six levels of headings:

```markdown
# 一级标题 / Heading 1
## 二级标题 / Heading 2
### 三级标题 / Heading 3
#### 四级标题 / Heading 4
##### 五级标题 / Heading 5
###### 六级标题 / Heading 6
```

## 文本样式 / Text Styling

- **粗体文本 / Bold text**
- *斜体文本 / Italic text*
- ***粗体加斜体 / Bold and italic***
- ~~删除线 / Strikethrough~~
- `行内代码 / Inline code`

## 列表 / Lists

### 无序列表 / Unordered List

- 项目 1 / Item 1
- 项目 2 / Item 2
  - 子项目 2.1 / Subitem 2.1
  - 子项目 2.2 / Subitem 2.2
- 项目 3 / Item 3

### 有序列表 / Ordered List

1. 第一步 / Step 1
2. 第二步 / Step 2
3. 第三步 / Step 3

### 任务列表 / Task List

- [x] 已完成任务 / Completed task
- [ ] 未完成任务 / Pending task
- [ ] 待办事项 / To-do item

## 链接和图片 / Links and Images

[链接文本 / Link text](https://github.com/你的用户名)

![图片描述 / Image description](static/assets/img/photo.png)

## 引用 / Blockquote

> 这是一段引用文本。/ This is a quote.
>
> 可以跨越多行。/ Can span multiple lines.

## 代码块 / Code Blocks

### 行内代码 / Inline Code

使用 `console.log()` 输出信息。/ Use `console.log()` to output information.

### 多行代码 / Multi-line Code

```python
def hello_world():
    print("Hello, World!")

def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)
```

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}
```

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

## 表格 / Tables

| 功能 / Feature | 状态 / Status | 优先级 / Priority |
|----------------|---------------|-------------------|
| Markdown | ✅ 完成 / Done | 高 / High |
| 数学公式 / Math | ✅ 完成 / Done | 高 / High |
| 分类筛选 / Category | ✅ 完成 / Done | 中 / Medium |
| 标签搜索 / Tags | ✅ 完成 / Done | 中 / Medium |

## 分割线 / Horizontal Rule

---

## 结语 / Conclusion

这就是 Markdown 的基本语法，更多用法请参考 [Markdown 官方文档](https://www.markdownguide.org/)。

This is the basic Markdown syntax. For more details, refer to the [Markdown Official Documentation](https://www.markdownguide.org/).
