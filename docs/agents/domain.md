# Domain Docs

## 布局与读取规则

本仓库采用 single-context：

- 根目录 GLOSSARY.md：领域术语。
- docs/adr/：架构决策记录。

探索代码前，读取术语表和涉及当前工作范围的 ADR。
文件不存在时直接继续；domain-modeling 在术语或决策确定后按需创建。

## 术语

Issue、设计提案、假设和测试名称使用术语表定义的词汇。
缺少所需概念时，判断是否为真实缺口，并交给 domain-modeling 处理。

## 决策冲突

提案与现有 ADR 冲突时，明确指出相关 ADR 及重新讨论的原因。
