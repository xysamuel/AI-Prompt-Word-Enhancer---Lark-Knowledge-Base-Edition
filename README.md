# AI 提示词增强器 · 飞书知识库版（Tampermonkey 用户脚本）

> 一条脚本，让 **DeepSeek / Kimi / 豆包** 瞬间拥有「方法论外挂」：  
> 输入任意需求 → 自动检索飞书多维表格 → AI 生成高质量提示词 → 一键复制并回填到输入框。

## 🌟 核心能力

| 功能 | 说明 |
| --- | --- |
| 🔍 **知识库检索** | 按关键词实时查询飞书多维表格，召回 0～3 条最相关方法论 |
| 🤖 **AI 二次润色** | 把「用户原始需求 + 方法论」喂给大模型，输出结构化提示词 |
| 📋 **自动复制回填** | 增强结果自动写入剪贴板并替换输入框原文，零打断流程 |
| 📚 **网页采集** | 任意页面 `Ctrl+Shift+C` 一键保存标题/正文/关键词到知识库 |
| ⚙️ **可视化配置** | `Ctrl+Shift+P` 弹出面板，填写飞书 & AI 参数即可使用 |
| 🎯 **多站点适配** | 已适配 DeepSeek、Kimi、豆包，其余站点自动降级为纯 AI 增强 |

---

## 🚀 2 min 上手

1. **安装脚本管理器**  
   [Tampermonkey 官网](https://www.tampermonkey.net/)（Chrome / Edge / Firefox 均支持）

2. **安装脚本**  
   

3. **配置飞书**  
   - 多维表格建表（字段：标题 / 内容 / 关键词 / 助手）  
   - 飞书开放平台创建「自建应用」→ 开通「多维表格」权限 → 获取 `App ID / Secret`  
   - 复制表格 URL，在脚本配置面板粘贴即可自动解析 `Base ID / Table ID`

4. **配置大模型**  
   支持任意 OpenAI-Compatible API（Moonshot / OpenAI / 本地 vLLM 等），填写 `Base URL + API Key + 模型名` 即可。

5. **开始使用**  
   在 DeepSeek / Kimi / 豆包输入框写好需求 → 点击「✨ 增强提示词」或按 `Ctrl+Enter` → 自动完成剩余步骤！

---

## 📖 快捷键速查

| 组合键 | 作用 |
| --- | --- |
| `Ctrl+Shift+P` | 打开配置面板 |
| `Ctrl+Shift+C` | 采集当前页面到知识库 |
| `Ctrl+Enter` | 触发提示词增强（需聚焦输入框） |

---

## 🛠️ 开发与构建

本仓库仅提供源码，**无需构建**；直接修改 `ai-prompt-enhancer.user.js` 头部 `// @version` 后拖入 Tampermonkey 即可热重载。

### 本地调试

```bash
# 克隆仓库
git clone https://github.com/YOUR_NAME/AI-Prompt-Enhancer-Feishu.git
cd AI-Prompt-Enhancer-Feishu

# 安装依赖（可选，仅用于 ESLint / Prettier）
npm install

# 代码风格检查
npm run lint
```

---

## 🤝 贡献指南

欢迎提 Issue / PR！  
请遵循 `.github/CONTRIBUTING.md` 中的规范；重大功能请先开 Discussion 讨论。

---

## 📝 许可证

MIT © 观澜话不多

---

## 🙏 致谢

- [Tampermonkey](https://www.tampermonkey.net/) 提供用户脚本运行时  
- [SweetAlert2](https://sweetalert2.github.io/) 美观的弹窗组件  
- 飞书开放平台 & Moonshot AI 提供稳定接口

---

如果本项目帮到了你，给个 ⭐ Star 支持一下哇～
