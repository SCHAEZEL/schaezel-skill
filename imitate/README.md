# Imitate Skill

> 让 AI 模仿任意领域最强的人，陪你一起思考问题。

## 功能

- **模式A（手动指定）**：指定两个人名，AI 同时扮演这两人回答问题
- **模式B（领域搜索）**：告诉 AI 一个领域，AI 自动搜索该领域最强的两个人
- **三人对话**：两位专家发言后，Claude 用大白话总结两人的核心分歧

## 安装

### Claude Code 用户

```bash
# 复制 SKILL.md 到你的 skills 目录
# Windows:
copy SKILL.md %USERPROFILE%\.claude\skills\imitate\

# 或者手动创建目录并复制文件
```

### OpenClaw 用户

```bash
npx clawhub@latest install SCHAEZEL/imitate-skill
```

## 使用方式

### 手动指定人名

```
/imitate 马斯克 库克 你认为小米汽车怎么样？
```

### 领域搜索

```
/imitate 投资 A股现在适合入场吗？
```

### 更多示例

| 输入 | 说明 |
|------|------|
| `/imitate 巴菲特 芒格 茅台值得投资吗？` | 指定人物 |
| `/imitate 周百见 田泽湘 如何提高口播能力？` | 短视频领域 |
| `/imitate 任泽平 杨德龙 买黄金还是定投沪深300？` | 投资领域 |

## 输出格式

```
## 马斯克 的观点

[以马斯克视角回答]

---

## 库克 的观点

[以库克视角回答]

---

## 💬 Claude 说人话

[总结两人的核心分歧，给出接地气的解读]
```

## 原理

1. 解析用户输入，提取人名或领域
2. 模式B下，使用 web_search 搜索该领域最强专家
3. 并行启动 2 个 Agent，分别扮演这 2 个人
4. 各自独立回答（不强制辩论）
5. 汇总呈现 + Claude 人话总结

## 相关

- 作者：SCHAEZEL
- GitHub：https://github.com/SCHAEZEL/imitate-skill
- Claude Code Skills 目录：`~/.claude/skills/`
