# 好爸妈 Skill｜AI 育儿教练

"不是让孩子更听话，而是让大人先稳住、看见孩子、守住边界。"

![Version](https://img.shields.io/badge/Version-v1.0.0-blue)
![License](https://img.shields.io/badge/License-Free%20Non--Commercial-red)
![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Claude%20Code%20%7C%20Codex%20%7C%20WorkBuddy-blue)
![Language](https://img.shields.io/badge/Language-中文%20%7C%20English-orange)

2 份育儿专家提示词 × 1 个完整 Agent Skill × 家庭背景卡 × 六步问诊流  
亲子冲突 / 作业崩溃 / 屏幕边界 / 隔代冲突 / 幼小衔接 / 长期教育规划

当前版本：v1.0.0。个人、家庭、公益和非商业教育场景免费使用；未经书面许可禁止商业使用。

中文 | [English](README_EN.md)

---

## 30 秒上手

只想复制提示词，直接看这里：

- [AI 育儿专家提示词](prompts/zh/parenting-expert-prompt.md)
- [家庭教育规划师提示词](prompts/zh/family-education-strategist-prompt.md)

想安装成 Claude Code / Codex / WorkBuddy 可调用的完整 skill：

```bash
git clone https://github.com/Lucius1105/ai-parenting-coach-skill.git
```

Claude Code：

```bash
mkdir -p ~/.claude/skills
cp -R ai-parenting-coach-skill/skills/ai-parenting-coach ~/.claude/skills/
```

Codex：

```bash
mkdir -p ~/.codex/skills
cp -R ai-parenting-coach-skill/skills/ai-parenting-coach ~/.codex/skills/
```

WorkBuddy：

```bash
mkdir -p ~/.workbuddy/skills
cp -R ai-parenting-coach-skill/skills/ai-parenting-coach ~/.workbuddy/skills/
```

装好后对 agent 说：

```text
使用 $ai-parenting-coach，我孩子 6 岁，准备上小学，平时奶奶带得比较多。最近写字和收拾书包总是拖，我一催就哭。先帮我判断问题，再给今晚能执行的方案。
```

---

## 这是啥

一句话：把一个家长的育儿困境，先整理成"家庭背景卡"，再用 AI 育儿教练帮你判断问题卡在哪里，最后给出能照着说、照着做的小方案。

它不做三件事：

- 不教你鸡娃
- 不教你用恐吓、羞辱、体罚压住孩子
- 不假装 AI 可以替代父母、医生、心理咨询师、社工或律师

它主要做六件事：

1. 帮大人先稳住情绪
2. 判断问题卡在发展层、状态层、关系层，还是行动层
3. 把任务拆到孩子能做到
4. 给父母、老人、老师可直接说的话术
5. 做 7 天微循环，而不是一次改完
6. 遇到安全、医疗、心理、法律红线时提醒找专业支持

---

## 为什么做这个

很多父母不是不爱孩子，而是在真实育儿现场里太累了。

孩子写作业崩溃、老人越界、伴侣不配合、手机规则执行不下去、幼小衔接焦虑、每天都在"我是不是又吼了孩子"的内耗里打转。

市面上很多育儿内容有两个问题：

- 要么太理论，讲完还是不知道今晚怎么说
- 要么太控制，把孩子当成需要被修理的问题

所以我们做了这个源码公开、个人家庭免费使用的 skill：把教练式提问、家庭系统视角、平和育儿方法和可执行话术打包成一个人人可用的 AI 育儿专家。

它的目标很简单：

> 帮更多父母少一点内耗，多一点稳定；帮更多孩子少一点被控制，多一点被看见。

---

## 两份提示词

这个仓库先公开两份可复制提示词。

### 第1份：AI 育儿专家提示词

路径：

```text
prompts/zh/parenting-expert-prompt.md
prompts/en/parenting-expert-prompt.md
```

适合：

- 亲子冲突
- 带娃计划
- 学习习惯
- 情绪爆发
- 屏幕边界
- 父母/老人/老师沟通

### 第2份：家庭教育规划师提示词

路径：

```text
prompts/zh/family-education-strategist-prompt.md
prompts/en/family-education-strategist-prompt.md
```

适合：

- 幼小衔接
- 小学阶段能力培养
- 隔代冲突
- 父母长期缺位补位
- 家庭系统边界
- 0-18 岁长期教育规划

---

## 适用年龄层

v1.0 覆盖 0-18 岁，但不是把所有孩子当成同一种孩子。

当前最成熟、最推荐的使用范围是 3-12 岁，尤其适合：

- 幼儿园到小学阶段的日常育儿
- 幼小衔接
- 作业、习惯、磨蹭、情绪爆发
- 父母和祖辈的育儿分歧
- 家庭规则、屏幕时间、亲子陪伴

其他年龄段也可以用：

- 0-3 岁：更适合做安全、节律、依恋和照护回应的梳理。
- 12-18 岁：更适合做尊重、协商、边界、隐私、学业压力和长期规划的整理。

如果问题涉及诊断、用药、自伤、伤人、家暴、虐待、严重拒学或持续心理危机，请优先找当地专业人士。

---

## 完整 Skill

真正给 agent 安装调用的是：

```text
skills/ai-parenting-coach/SKILL.md
```

Skill 内部还带两份脱敏提示词模块：

```text
skills/ai-parenting-coach/references/parenting-expert-prompt.md
skills/ai-parenting-coach/references/family-education-strategist-prompt.md
```

主流程会先判断用户问题类型：

- 日常育儿问题 → 调用 `parenting-expert-prompt.md`
- 长期规划 / 隔代冲突 / 家庭系统问题 → 调用 `family-education-strategist-prompt.md`

---

## 强制流程：先补齐家庭背景卡

这是这个 skill 最重要的设计。

所有孩子和家庭都不一样，所以 agent 不能一上来就给建议。用户必须先补齐：

- 孩子：年龄、性别、年级/阶段、性格、兴趣、优势、最近困扰
- 主要照护者：谁陪得最多，谁负责规则，谁容易情绪失控
- 家庭成员：父母、祖辈、老师或其他重要成年人分别扮演什么角色
- 当前问题：最近一次具体事件发生了什么
- 用户目标：想解决当下冲突、做带娃计划、改善学习习惯，还是做长期规划
- 红线信号：有没有安全、健康、学校、家庭暴力、严重心理风险

背景不足时，agent 应先问，不应直接给泛泛建议。

---

## 使用场景

### 场景1：作业崩溃

```text
使用 $ai-parenting-coach，孩子 8 岁，一写作业就哭，说自己不会。我越催越急，最后总是吼。帮我处理今晚这一次。
```

### 场景2：幼小衔接

```text
使用 $ai-parenting-coach，孩子 6 岁，准备上小学，平时奶奶带得多。帮我做一个不鸡娃的幼小衔接方案。
```

### 场景3：隔代冲突

```text
使用 $ai-parenting-coach，奶奶老是在孩子专注画画的时候打断，还会说画得不像。我怎么沟通？
```

### 场景4：屏幕边界

```text
使用 $ai-parenting-coach，孩子沉迷短视频，老人一带娃就给手机。我不想吵架，但要把规则立起来。
```

### 场景5：父母协同

```text
使用 $ai-parenting-coach，我和伴侣教育观念不一致，他觉得我太惯孩子，我觉得他太凶。孩子夹在中间。
```

---

## 脱敏说明

这个公开版来自两份内部提示词的脱敏重写：

- `parenting-advisor`：贡献了"允许、陪伴、兜底、放手"和高质量陪伴工具
- `首席教育规划师_Skill_v4.md`：贡献了家庭系统视角、六步问诊流、隔代冲突 SOP 和长期教育规划

原始文件包含具体客户、孩子、家庭成员和生活细节，不能公开。这个仓库只保留方法，不保留任何真实家庭信息。

---

## 不适用范围

这个 skill 不能替代医生、心理咨询师、社工、律师或学校专业支持。

遇到自伤、伤人、严重拒学、疑似抑郁、疑似 ADHD、疑似自闭谱系、家暴、虐待、抚养权争议、用药诊断等问题，请优先找当地专业人士或应急资源。

---

## 免费授权与禁止商业使用

这个项目免费公开给家长使用，不卖课，不设门槛。

你可以：

- 给自己家庭使用
- 分享给朋友和其他家长
- 用于公益、学校、社区、非商业教育场景
- 在保留署名和项目链接的前提下学习、复制和改编

未经作者书面许可，不得将本项目或衍生版本用于商业用途，包括但不限于：

- 包装成付费课程、训练营、咨询服务、陪跑服务
- 包装成商业软件、智能体、SaaS、插件、提示词库、会员资料
- 改名、改包装后收费分发
- 用于商业广告、商业获客或商业交付
- 用于模型训练、数据集构建或闭源商业产品

发现未经授权商业使用，作者保留追究责任的权利。完整条款见 [LICENSE](LICENSE)。

---

## 支持与打赏

如果这个 skill 帮你少吼了一次，帮孩子少受一次委屈，或者让你对孩子的长期教育更有方向，欢迎请我喝杯咖啡。

孩子的教育是一个长期、重大、值得认真投入的项目。一节私教课常常 200 元起步；如果你觉得这个提示词对你的家庭长期有价值，可以随缘支持我们继续维护、升级，帮助更多孩子和家庭。

我也是一个孩子的爸爸，也希望用正当创造，光明正大地为自己的孩子挣一些学费。感谢你的支持和投资。

![微信打赏二维码](assets/wechat-pay-qr.jpg)

---

## 作者与全渠道

作者：徐沛霖 / 阿徐教练 / 雨后甘霖创始人

全渠道名称：阿徐教练｜雨后甘霖

公众号 / 视频号：阿徐教练

---

## 版本与更新

- 当前版本：[v1.0.0](VERSION)
- 更新日志：[CHANGELOG.md](CHANGELOG.md)
- 授权条款：[LICENSE](LICENSE)

如果它帮到了你，欢迎：

- Star 这个仓库
- 分享给需要的爸爸妈妈
- 提 Issue 反馈真实场景
