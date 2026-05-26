# WeChat OA Prepublish Auditor Skill

一个用于 **微信公众号文章发布前合规审核** 的 Codex Skill。

它把微信公众平台规则中心、公众号运营规范，以及诱导行为、违规导流、过度营销、不实信息、标题煽动夸大误导等官方案例，整理成可复用的发文前审核流程。

> 非微信官方项目，非法律意见。最终以微信公众平台最新规则、相关法律法规和平台实际审核结果为准。

## 适合谁用

- 公众号作者、编辑、运营。
- 使用 AI 辅助写公众号文章的人。
- 需要在发布前检查标题党、引流、二维码、课程广告、健康/金融/政策内容风险的人。
- 想把“发文前合规审核”变成固定工作流的人。

## 能检查什么

- 标题是否煽动、夸大、恐吓、误导、假借官方/机密。
- 正文是否涉及不实信息、侵权、转载授权、隐私、低俗、赌博荐彩、非法物品、封建迷信等。
- 是否存在诱导关注、分享、点击、扫码、加群、加个人微信、跳小程序或第三方平台。
- 课程、广告、商业合作、金融、健康、医疗、政策等内容是否有夸大承诺或披露不足。
- AI 内容是否存在批量生成、洗稿、搬运、模板化低价值、自动发布教程等风险。
- 封面图、二维码、引导图、小程序卡片、截图里的文字和视觉风险。

## 安装

复制整个 skill 文件夹：

```text
skills/wechat-oa-prepublish-auditor
```

到你的 Codex skills 目录：

```text
~/.codex/skills/wechat-oa-prepublish-auditor
```

Windows 示例：

```text
C:\Users\<你的用户名>\.codex\skills\wechat-oa-prepublish-auditor
```

最终结构应该是：

```text
~/.codex/skills/wechat-oa-prepublish-auditor/
  SKILL.md
  agents/
    openai.yaml
  references/
    wechat-oa-rules.md
    audit-test-cases.md
```

安装后重启 Codex 或新开会话。

## 使用示例

```text
用 $wechat-oa-prepublish-auditor 帮我审核这篇公众号文章，看看标题、正文、二维码引流和课程转化有没有违规风险。
```

也可以直接说：

```text
帮我做公众号发文前合规审核。
```

如果 skill 被正确识别，审核输出会包含：结论、风险等级、命中规则、问题片段、修改建议、可替代表达、未覆盖范围、发布前检查项。

## 规则来源

- 微信公众平台规则中心：<https://mp.weixin.qq.com/webpoc/ruleCenter?type=oa>
- 微信公众平台运营规范：<https://mp.weixin.qq.com/mp/opshowpage?action=newoplaw>
- 诱导行为案例：<https://mp.weixin.qq.com/s/mcnPfmrf7m0fd8jCGkw7EQ>
- 违规导流案例：<https://mp.weixin.qq.com/s/W0p4gEMj7yfhlkUm18MC9A>
- 过度营销案例：<https://mp.weixin.qq.com/s/Te--qgLaGpq8d9IsY__9lw>
- 不实信息案例：<https://mp.weixin.qq.com/s/xdG35DasOFxb-GCVhU76Mw>
- 煽动、夸大、误导案例：<https://mp.weixin.qq.com/s/Cm3Wj0kCIihC48zAmvxQhg>
- 标题煽动夸大误导案例解析：<https://mp.weixin.qq.com/s/9WFjzGCJSrO3d1qk5maMBw>

## 更新建议

微信规则会变化。建议在这些情况下重新核验官方规则中心：

- 准备批量发布或搭建长期自动化发文流程。
- 涉及金融、健康、医疗、政策、法律、婚恋、按摩、荐彩等高风险领域。
- 账号收到处罚、警告、限流或投诉。
- 距离上次规则核验超过 30 天。

## License

MIT License. See [LICENSE](LICENSE).
