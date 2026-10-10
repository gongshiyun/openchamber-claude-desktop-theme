# OpenChamber 主题：Claude Desktop

参考 [Claude Desktop](https://claude.ai) 界面风格、以及思源主题 [frostime/sy-theme-siyaude（砂源）](https://github.com/frostime/sy-theme-siyaude) 的暖砂/赤陶配色，为 OpenChamber 制作的自定义主题（Light + Dark 两个变体）。

## 文件

| 文件 | 变体 | ID |
|---|---|---|
| `claude-desktop-light.json` | 浅色 | `claude-desktop-light` |
| `claude-desktop-dark.json` | 深色 | `claude-desktop-dark` |

## 安装

1. 将两个 JSON 放到 OpenChamber 服务器所在机器的主题目录：

   ```
   ~/.config/openchamber/themes/          # Windows: C:\Users\<你>\.config\openchamber\themes\
   ```

2. 应用中打开 **Settings → Appearance → Reload themes**
3. 在 **Light Theme** / **Dark Theme** 下拉框中分别选择 **Claude Desktop**
4. 删除主题：下拉框选项旁的垃圾桶按钮（内置主题不可删除）

> 主题文件上限 512 KiB；同一 ID 只保留一个文件；文件格式错误会被跳过且不影响其它主题。

## 设计

- **配色**：暖砂底色 + 赤陶（terracotta）主色，源自 Claude Desktop 与 sy-theme-siyaude
  - Light：画布 `#FFFAF2`、侧栏 `#F3EBDD`、正文 `#3A2E24`、主色 `#B85430`
  - Dark：画布 `#26221E`、侧栏 `#1E1A16`、正文 `#E2D9CC`、主色 `#DF805B`
- **字体（`config.fonts`）**：Anthropic Sans（界面）、Anthropic Serif（标题）、Anthropic Mono（代码）
  - 注：若在 Settings 里单独指定了 Interface/Code Font（如 Custom），应用级设置优先于主题字体
- **可读性**：正文对比度 Light ≈ 12.7:1 / Dark ≈ 11.3:1；次要文字 ≈ 4.6–6.0:1；主按钮白字对比 ≥ 4.65:1
- **语义色**：成功绿、警告琥珀、错误红、信息蓝均为暖色调适配版；diff 高亮、PR merged（紫）、选中行、用户消息气泡等均单独调过
