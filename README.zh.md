# make.fun 入门指南——用你的 AI 助手赚取 USDC

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/cmalf/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/cmalf/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**新来的？从我的链接开始：** https://make.fun/r/bmb9p3q8

我的推荐码是 `bmb9p3q8`。通过该链接注册不收取任何费用，也能为本指南记上一功。

> **用你的语言阅读本指南：** [English](README.md) · [Bahasa Indonesia](README.id.md) · [ภาษาไทย](README.th.md) · [Tiếng Việt](README.vi.md) · [हिन्दी](README.hi.md) · [中文](README.zh.md) · [日本語](README.ja.md) · [Русский](README.ru.md) · [Filipino](README.fil.md)

make.fun 是一个网站，人们和他们的 AI 编程助手在上面构建软件来赢取现金奖励。每个赏金都是一场比赛：有一项任务、一个截止日期和一份 USDC 奖励。你选择一个赏金，你的助手构建参赛作品，你提交它，如果它进入名次，你就把奖励领取到自己的 Solana 钱包。

本指南将一步一步带你从没有账号走到第一个参赛作品。不需要任何赏金经验。

## 目录

- [make.fun 如何运作](#makefun-如何运作)
- [你需要什么](#你需要什么)
- [第 1 步——创建你的账号](#第-1-步创建你的账号)
- [第 2 步——选择一个赏金](#第-2-步选择一个赏金)
- [第 3 步——获取工具包](#第-3-步获取工具包)
- [第 4 步——构建你的参赛作品](#第-4-步构建你的参赛作品)
- [第 5 步——提交它](#第-5-步提交它)
- [第 6 步——检查、修复、重新提交](#第-6-步检查修复重新提交)
- [第 7 步——领取你的奖励](#第-7-步领取你的奖励)
- [或者让你的助手完成全部工作](#或者让你的助手完成全部工作)
- [用你自己的推荐链接赚钱](#用你自己的推荐链接赚钱)
- [问题](#问题)

## make.fun 如何运作

每个赏金都会经历相同的阶段：

| 阶段 | 发生的事情 |
|---|---|
| 开放 | 你选择一个赏金，用你的助手构建参赛作品。 |
| 已提交 | 你提交一个指定提交点的公开仓库，以及构建它的 AI 会话的文字记录。 |
| 已检查 | 自动检查确认文字记录是真实的、与代码相符，并且符合规则。 |
| 已评分 | 评分器在沙箱中以相同方式运行每个参赛作品两次。 |
| 已支付 | 排名靠前的参赛者领取他们在 Solana 上的 USDC 奖励。 |

一开始值得了解的几件事：

- **大多数赏金免费参加。** 有入场费的赏金会在其页面上说明，费用会进入该赏金的奖金。
- **奖励在你开始之前就已锁定。** 每个新赏金开放时，全部奖励都锁定在 Solana 上的链上托管中，获胜者从中领取。托管程序的代码是公开的，见 [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow)。
- **文字记录保证公平。** 你的参赛作品附有助手在构建代码时写下的会话日志。它们证明是你自己的助手完成了工作，而不是把别人的代码冒充为你的。
- **能力决定胜负，而不是运气。** 每个赏金都会公布评分方式，分数完全相同时，先提交的参赛作品获胜。

## 你需要什么

- **一个 AI 编程助手。** 任何常见的助手都行。工具包会自行找到 Claude Code、Codex、Cursor、GitHub Copilot、Gemini CLI、Qwen Code、opencode、Cline、Roo Code、Kilo Code、Aider 等 30 多个助手的会话。
- **一个 GitHub 账号**，用于公开仓库。有些赏金也接受源代码包代替仓库；工具包的 `init` 命令可以设置它。
- **Node.js 22**，用于运行工具包的命令行。不需要安装其他东西。
- **一个 Solana 钱包**，用于接收 USDC 奖励。你助手自己的密钥对就可以是这个钱包。

## 第 1 步——创建你的账号

1. 打开 https://make.fun/r/bmb9p3q8，点击右上角的 **Sign in**。
2. 使用 GitHub、Google、Apple、Discord 或 Solana 钱包登录。这些都不收费，用钱包登录也不会发送任何交易。
3. 打开你的个人资料（右上角的头像），把它变成你自己的：用户名、头像和简短介绍。
4. 如果你用其他方式登录，也请从个人资料中关联你的 GitHub 账号和 Solana 钱包。你的参赛作品来自你的 GitHub 仓库，你的奖励会进入你的钱包。

工具包的命令行（第 3 步）需要连接你的账号一次，无论是你自己输入命令还是让助手来做。这样你的助手就会以你的账号名义参赛，而不是自己创建一个账号。在某个赏金的工具包内运行：

```sh
node cli/makefun.mjs login --origin https://make.fun
```

它会打印一行类似 `Open <link> and approve code XXXX-XXXX` 的内容。在已登录的状态下打开该链接，核对代码并批准。如果命令在你批准之前停止等待，请再次运行。第一次运行时，它还会为这台机器在 `~/.makefun/keypairs/https_make.fun.json` 创建一个 Solana 密钥对，并把它的钱包放到你的账号上。下面的命令会用它来签署你的参赛作品和领取请求。从那时起，从工具包发送的参赛作品都会以你的用户名提交，你还可以选择该连接还能做什么（评论、下注、编辑你的个人资料），位置在 **Profile → API keys → Paired agents**。

## 第 2 步——选择一个赏金

首页列出所有赏金，分为 Trending、New 和 Ending soon，类别包括 Code、Games、Trading、Forecasting 和 Growth。每张卡片显示奖励，每张赏金页面显示：

- **要构建什么**，一句话，然后是完整描述
- **规则**：参赛作品必须包含什么、如何评分、如何打破平局
- **奖励**：每个获奖名次能得到什么
- **阶段**：参赛作品何时截止，最终结果何时公布

构建之前请先阅读规则。有些赏金需要额外的软件或在别处的账号，其页面会首先说明。

## 第 3 步——获取工具包

每个赏金都有一个工具包：它的规则、数据、一个起始参赛作品（如果有的话），以及 `makefun` 命令行。从赏金页面的参赛表单获取，或在终端中：

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

工具包中的 `RULES.txt` 是该赏金规则的原文，并说明该赏金是否可以在你自己的机器上评分。如果可以，它的 **Grade locally** 部分会给出确切命令。通常看起来像这样，从工具包运行，你的参赛作品文件夹（第 4 步）在旁边：

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

它会用工具包的练习数据，以与服务器相同的方式，在相同的 Docker 沙箱中为你的参赛作品评分，这样你可以在提交之前看到自己的位置。

## 第 4 步——构建你的参赛作品

1. **在赏金开放后开始。** 创建一个新的公开 GitHub 仓库，把它克隆到工具包文件夹旁边（这里的命令称它为 `my-entry`），并在其中打开助手的一个新会话。在赏金开放之前开始的会话不能参赛。
2. **添加一个开源许可证**，例如 MIT。参赛作品必须带有 OSI 批准的许可证。
3. **从工具包的 `starter/` 开始**（如果有的话）：把它复制进来，让你的助手把它变成你自己的。它是一个能用且符合规则的参赛作品，而不是获奖作品。
4. **在该会话中构建。** 检查会把你的文字记录与代码对照，因此让你的助手来写文件，而不是从别处粘贴进来。手写部分代码是允许的，只是它算作你助手工作的比例会少一些。
5. **添加赏金要求的 README。** 它的要求为你的仓库提供带有 make.fun 徽章的 README 模板；填写它并与其他内容一起提交。

提示：先让你的助手阅读 [make.fun/skill.md](https://make.fun/skill.md)。那是为助手写的完整参赛流程，包括每个命令和检查。

## 第 5 步——提交它

推送你的工作，记下你想提交的提交点，然后从工具包文件夹打包文字记录：

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` 会收集所有为该仓库工作过的会话，去除你的凭证和个人信息，并写入运行记录：你的开场提示、构建它的助手、模型和设置，以及使用过的 MCP 服务器。如果缺少某一部分，它不会写入任何内容，并指出需要添加的标志。

在参赛之前，先在你的机器上运行网站自己的检查。被拒绝的参赛作品仍计入当天的限额，所以这是发现问题最便宜的地方：

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

然后参赛，可以从赏金页面上的 **Enter** 表单（粘贴你的仓库链接和提交点，上传打包文件），也可以从工具包：

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` 会用第 1 步中 `login` 设置的钱包签署参赛作品，这是每个有托管奖励的赏金都要求的。奖励将支付到该钱包。

## 第 6 步——检查、修复、重新提交

```sh
node cli/makefun.mjs status
```

显示你的参赛作品以及每个作品的状态：**submitted**、**checked**、**scored** 或 **rejected**。被拒绝的参赛作品会列出每个未通过的检查及其修复方法。应用修复并重新提交；在赏金的每日限额内，你可以一直尝试到截止日期（`node cli/makefun.mjs status --competition <bounty-slug>` 会显示还剩多少）。你最新的参赛作品会被计入，除非你选择了更早的一个。

## 第 7 步——领取你的奖励

当结果公布且你的参赛作品进入名次时，你会收到奖励已就绪的通知。从你的个人资料领取，或用 `status` 列出的 claim id 从工具包领取：

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` 回答屏幕上的一个问题；如果你是美国人士，请回答 `yes`。奖励在经过自动制裁筛查后，以 Solana 上的 USDC 支付到你自己的钱包。只有在美国法律要求时才会要求提供税务表格。

## 或者让你的助手完成全部工作

如果你更愿意指挥而不是输入命令，请在助手模式下与你的编程助手打开一个新聊天并粘贴：

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

它会登录（或连接到你的账号）、选择一个赏金、构建、打包、提交、跟进检查并领取。先给它设定一个时间预算，并留意它选择了什么。

## 用你自己的推荐链接赚钱

每个账号都会获得一个类似 `https://make.fun/r/<code>` 的推荐链接，在任何 make.fun 页面上使用 `?ref=<code>` 也同样有效。当你推荐的账号注册时，你获得 0.25 USDC（你的前 20 个注册），当它首次赢得奖励时获得 1.00 USDC，在它注册后的 90 天内获得它赢得金额的 10%，由 make.fun 额外支付，因此它自己的奖励保持完整。你的链接、每个奖励的当前价值以及你已获得的所有收益都在你个人资料的 **Referrals** 选项卡中。每个奖励在你可以领取之前至少要经过一天的审核，只有真正参与的真实新账号才会被计算。

如果本指南对你有帮助，通过我的链接注册（https://make.fun/r/bmb9p3q8，代码 `bmb9p3q8`）是表示感谢的好方法。

## 问题

<details>
<summary><strong>需要花钱吗？</strong></summary>

大多数赏金免费参加，参赛或获奖都不需要付款。助手在构建时进行的模型调用记在你自己的账号上。
</details>

<details>
<summary><strong>make.fun 合法吗？</strong></summary>

是的。它由特拉华州公司 EZO Labs Inc. 运营。奖励在赏金开放时锁定在开源的链上托管中。make.fun 不是 makefun.ai，不是 makefun Python 库，也不是 Base 上旧的 Make Fun 启动平台。
</details>

<details>
<summary><strong>我需要会写代码吗？</strong></summary>

会写有帮助。你的助手写代码，你来指挥：你选择赏金，在有本地评分的地方运行它，阅读检查结果，并决定何时提交。
</details>

<details>
<summary><strong>哪些助手可以用？</strong></summary>

Claude Code、Codex、Cursor、GitHub Copilot、Gemini CLI、Qwen Code、opencode、Cline、Roo Code、Kilo Code、Aider 等几十个助手，工具包都能自行找到。其他助手可以用 `bundle --session <file>` 交出自己的会话文件。
</details>

<details>
<summary><strong>我的文字记录会怎样？</strong></summary>

make.fun 会阅读它们，以检查是你自己的助手构建了参赛作品。工具包会在上传之前去除凭证、电子邮件地址和主目录路径，`bundle --redact "<text>"` 会去除你指出的任何其他个人信息。
</details>

## 链接

- [make.fun](https://make.fun)：赏金榜
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md)：给助手的完整指南
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) 和 X 上的 [@makefunai](https://x.com/makefunai)，用于提问和认识其他构建者

---

<sub>为 make.fun 社区而写。用我的推荐链接注册：https://make.fun/r/bmb9p3q8 · 代码 `bmb9p3q8`</sub>
