# 🔍 Playbook 自审模板

> **使用场景**：定期对 ai-playbook 仓库本身进行质量审核
> **使用方式**：在任意 AI 对话中粘贴以下内容
> **建议频率**：每次 playbook 有重大更新后执行一次

---

请对以下仓库进行完整质量审核：

📂 https://github.com/loveil381/ai-playbook

## 审核要求

1. **依次抓取以下文件完整阅读**：
   - `https://raw.githubusercontent.com/loveil381/ai-playbook/main/CTO-PLAYBOOK.md`
   - `https://raw.githubusercontent.com/loveil381/ai-playbook/main/playbook/part1-core.md`
   - `https://raw.githubusercontent.com/loveil381/ai-playbook/main/playbook/part2-extend.md`
   - `https://raw.githubusercontent.com/loveil381/ai-playbook/main/README.md`
   - 所有 `prompts/` 目录下的文件

2. **按以下维度审核**：
   - **一致性**：入口文件目录 vs 分卷实际章节是否匹配；prompt 模板引用的 URL 是否全部指向正确的分卷文件
   - **完整性**：拆分过程中是否丢失内容；所有交叉引用（"详见第X章"）是否附带了正确的 Part 链接
   - **可用性**：prompt 模板粘贴后 CTO agent 是否能无障碍启动（有 [REPO] 占位符、有仓库 URL、有明确的首步指令）
   - **时效性**：模型列表是否与你了解的最新工具版本一致；外部链接（agentskills.io、GitHub 仓库）是否仍然可访问
   - **风格一致性**：快捷命令表反引号、emoji 使用、章节编号格式是否统一
   - **编码**：是否有异常问号残片或 mojibake

3. **输出格式**：
   按严重程度分类（🔴 Critical / 🟠 Major / 🟡 Minor / 🔵 Innovation），每条含具体文件名 + 问题描述 + 建议修复方案。最后输出优先级排序的变更清单。
