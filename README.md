# xingtu-bci · AI 协作坏例集（Bad Case Index）

> 本地构建中 · 尚未推送公开。记录「人跟 AI 协作时踩过的坑」，每条 = 现象 → 根因 → 可执行预防。

[![License: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](./LICENSE) ![状态](https://img.shields.io/badge/状态-本地构建-lightgrey)

## 一句话定位

把 AI 协作中的返工、误判、泄漏、假成功沉淀成可复用的护栏——**一个坏例 = 一条教训 + 一条可执行的预防**，不写空话。

## 核心原则：只出机制，不出实体

这是本仓的生死线。坏例的价值在**判断机制**（当时怎么想错的、怎么防），不在**项目实体**（哪个接口、哪个仓、哪个人）。因此：

- ✅ 收录：错误模式、根因分类、可执行的预防动作、判断规则、自查问句。
- ❌ 不收录：接口名 / 类名 / 内部仓名 / 内网域名 / 客户名 / 人名 / 具体业务数据 / commit hash / 内部问题编号。

一个坏例脱敏后若失去现场感，靠**保留决策层次与时间线**补，不靠保留实体补。

## 案例来源（SSoT）

本仓案例来自维护者长期维护的坏例索引（现象→根因→预防三段式），**均为脱敏改写后的通用机制**：

- 编造第三方机制 / 二手数字当依据
- 并发写覆盖 / 成功回执不等于结果正确
- 同一事实多副本各自腐烂 / 枚举类事实内联复述
- 中文内容用 grep 校验的假阴性
- 正文泄露内部元信息（AI 出稿指纹）
- 共享方法改动的边界判断与「新增优于修改」原则

外部项目若涉及，只做形态与机制对照，标 `public-source` + 原文链接 + 核对日期，不包装成亲历实测。

## 与相邻仓的边界

| 仓 | 管什么 | 不管什么 |
|---|---|---|
| `xingtu-agent` | Agent 落地场景案例与决策链 | 不专门收「协作出错」的坏例 |
| `xingtu-testting` | AI 测试的问题与判断 | 不记录协作流程的失误 |
| **xingtu-bci**（本仓） | AI 协作失误的模式与可执行护栏 | 不做测试方法论、不做 Agent 场景复盘 |

## 核心内容

- **坏例卡**：统一模板，现象 → 根因 → 预防 → 证据 → 脱敏自检。
- **护栏清单**：从坏例升级出的可执行规则（何时该变成脚本 Gate / hook / 硬规则）。
- **升级路径**：坏例先「仅记录」，证据够了再提为硬红线——不轻易把一条教训变成全局禁令。


## 归属与导航

本仓属于[行途 XingTu 开源矩阵](https://github.com/xingtu1996)的案例集分区，主题独立维护；[名片仓](https://github.com/xingtu1996)只做索引，不复制本仓内容。

案例集分四仓，按边界分工、互相引用：

- [xingtu-testting](https://github.com/xingtu1996/xingtu-testting) · AI 测试
- [xingtu-bot](https://github.com/xingtu1996/xingtu-bot) · Bot 形态
- [xingtu-agent](https://github.com/xingtu1996/xingtu-agent) · Agent 落地
- [xingtu-bci](https://github.com/xingtu1996/xingtu-bci) · 协作坏例

## 快速开始

```bash
git clone <仓库地址> xingtu-bci
cd xingtu-bci
# 模板在 cases/_TEMPLATE.md，已收录案例在 cases/public/
```

新增案例先读 [`cases/_TEMPLATE.md`](cases/_TEMPLATE.md)，按状态标注与证据来源填写。

## 案例状态标注（全仓统一）

| 状态 | 含义 |
|---|---|
| `design` | 仅设计/设想，未验证 |
| `public-source` | 公开资料整理，非本仓实测，带链接与核对日期 |
| `verified` | 本机实测，有可核对证据 |
| `production` | 生产环境在用 |

## 入库规范（硬门槛）

1. 实体脱敏：接口名 / 内部仓名 / 域名 / 人名 / 客户名 / 问题编号 / commit hash 一律不入库。
2. 时间脱敏：绝对日历改相对周次，避免反推项目周期。
3. 数量脱敏：不写可定位的规模数字。
4. 数字标注来源与验证程度；二手数据不作为判据。
5. 每条必须可执行——「以后注意」不算预防，「改前先枚举全部调用方」才算。

## 许可证

[MIT](./LICENSE) · 行途 XingTu

## 作者与联系

行途 XingTu（工程署名）· 微信搜索关注：**行途技术手记**
