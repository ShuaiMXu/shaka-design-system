# Shaka Design System

供 AI Agent 和设计师共同查阅的设计规则库，统一公众号、PPT、小红书和邮件等内容的视觉语言。

本仓库只维护共享设计规范，不生成 HTML，也不包含业务排版或发布流程。

## 内容

- `SKILL.md`：设计系统说明、引用方式、维护流程与职责边界。
- `references/themes.md`：5 套主题配色。
- `references/fonts.md`：标题、正文及等宽字体层级。
- `references/components.md`：callout、stat、pillar、figure、tag 等通用组件。
- `references/principles.md`：约束式设计原则。

## 安装与引用

将仓库放入所用 Agent 的 Skills 目录，例如：

```bash
git clone https://github.com/ShuaiMXu/shaka-design-system.git ~/.claude/skills/shaka-design-system
```

若目标目录已经存在，请先核对已有内容，不要直接覆盖。

下游 Skill 在生成内容前读取 `SKILL.md` 和 `references/` 中的规则；本 Skill 不主动触发内容生成。运行环境中的挂载路径可能不同，引用时以实际 Skill 根目录为准。

## 与公众号 Skill 的关系

- 本仓库维护可复用的视觉规则。
- [gzh-design-skill](https://github.com/ShuaiMXu/gzh-design-skill) 独立维护公众号排版、校验和草稿发布流程；当前仍有自己的主题组件库，独立建仓不意味着已经完成两者的规则整合。
- `ai-tech-wechat-writer` 是本设计系统文档中列明的公众号下游 Skill；它与 `gzh-design-skill` 不是同一个 Skill。

## 维护

修改共享规则前检查下游影响，在相应文件记录变更日期和原因。删除组件或重命名变量时，同步迁移受影响的下游引用。

## 来源与许可

本设计系统从 [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill) 引用、迁移并抽取部分设计规则和组件，保留原始 Skill 文档中的来源说明。上游目前采用 AGPL-3.0，本仓库延续该许可证，完整文本见 [LICENSE](LICENSE)，整理和修改说明见 [NOTICE.md](NOTICE.md)。
