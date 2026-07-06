# Calm Parenting Coach

平和育儿教练，一个给父母、照护者、老师和教练使用的 AI Agent Skill。

它帮助你把育儿问题从"怎么管孩子"转成"孩子和成人此刻各自卡在哪里"，再生成今晚就能执行的小方案。

核心方向：

- 少吼、少羞辱、少鸡娃
- 多看见、多协商、多练习
- 先稳住大人，再稳住孩子
- 既尊重孩子，也保留清楚边界

## 适合处理

- 孩子写作业崩溃、拖延、磨蹭
- 情绪爆发、哭闹、顶嘴、亲子冲突
- 屏幕时间、游戏边界、学习习惯
- 周末、旅行、寒暑假带娃计划
- 父母、老人、老师之间的沟通协调
- 家长不想再吼，但不知道还能怎么做

## 不适合处理

这个 skill 不能替代医生、心理咨询师、社工、律师或学校专业支持。

遇到自伤、伤人、严重拒学、疑似抑郁、疑似 ADHD、疑似自闭谱系、家暴、虐待、抚养权争议、用药诊断等问题，请优先找当地专业人士或应急资源。

## 安装

克隆仓库：

```bash
git clone https://github.com/Lucius1105/calm-parenting-coach.git
```

安装到 Claude Code：

```bash
mkdir -p ~/.claude/skills
cp -R calm-parenting-coach/skills/calm-parenting-coach ~/.claude/skills/
```

安装到 Codex：

```bash
mkdir -p ~/.codex/skills
cp -R calm-parenting-coach/skills/calm-parenting-coach ~/.codex/skills/
```

安装到 WorkBuddy：

```bash
mkdir -p ~/.workbuddy/skills
cp -R calm-parenting-coach/skills/calm-parenting-coach ~/.workbuddy/skills/
```

## 使用示例

```text
使用 $calm-parenting-coach，孩子写作业一写就崩溃，我不想再吼了，帮我设计今晚的处理方式。
```

```text
使用 $calm-parenting-coach，周末我一个人带 6 岁孩子，帮我做一个不鸡娃也不失控的安排。
```

```text
使用 $calm-parenting-coach，老人总用短视频哄孩子，我怎么沟通才不撕破脸？
```

## 方法骨架

这个 skill 默认按六步输出：

1. 一句话判断：问题主要卡在发展层、状态层、关系层，还是行动层。
2. 先稳住谁：先稳成人、孩子、关系，还是规则。
3. 今晚动作：1-3 个立即可做的小动作。
4. 可直接说的话：给家长自然话术。
5. 7 天微循环：只设一个目标、一个动作、一个观察指标。
6. 需要警惕：出现哪些信号应找专业支持。

## 开源与支持

本项目免费开放，采用 MIT License。

如果它帮到了你，欢迎：

- Star 这个仓库
- 分享给需要的爸爸妈妈
- 提 Issue 反馈真实场景
- 后续咖啡打赏入口补上后，可随缘支持

愿更多父母少一点内耗，多一点稳定；更多孩子少一点被控制，多一点被看见。
