# 原心项目管理插件

独立项目仓库与插件市场。版本：`0.1.0-alpha.2`；固定测试标签：`v0.1.0-alpha.2`。连接 `https://projects.yuanxininsight.com/mcp`，无需本机运行服务。

## 首次安装

在已安装Codex CLI的终端执行：

```bash
codex plugin marketplace add chenhebuaa/yuanxin-project-management-plugin --ref v0.1.0-alpha.2
codex plugin add feishu-project-insights-lite@yuanxin-project-management
codex mcp login feishu-project-insights-lite
```

按浏览器提示以本人飞书账号登录，然后新建Codex对话。

## 从旧试用包迁移

此前若从日历市场安装过项目插件，先执行 `codex plugin remove feishu-project-insights-lite@yuanxin-insight`；本机预览使用 `codex plugin remove feishu-project-insights-lite@feishu-project-insights-lite-local`。再按上方添加独立市场并安装，已有有效授权时无需重复login。连接标识保持不变，避免搬运或导出令牌。

日历用户可单独将原市场重新固定到日历版本：

```bash
codex plugin marketplace remove yuanxin-insight
codex plugin marketplace add chenhebuaa/zhijian-calendar-plugin --ref v1.1.0
codex plugin add zhijian-calendar@yuanxin-insight
```

后续两个插件各自安装、更新和发布，不要求同时升级。

## 试用验收

试用成员须在此飞书应用的可用范围内，并由管理员以该应用的open_id加入服务准入。未准入时请联系管理员，不要借用他人账号。准入只允许使用插件，文档和群聊仍按本人飞书权限读取；普通成员不能保存项目配置。

依次验证：

1. “用原心项目管理插件列出可查询的项目。”
2. “分析幻师COMMUNE的最新进展、客户尚未解决的问题和风险。”核对可读文档来源及读取缺口。
3. 使用本人确实无权的已配置资料验证权限提示，不应出现正文。若暂无这样的资料，记录为未验收。

群聊参与分析，但回答不罗列消息ID或单列群聊证据。当前不是增量分析，PDF、图片、附件等读取有限，序列结束不代表资料全部覆盖。当前仅完成部署和连接准备，同事本人权限及连续试用仍须实际验收。

后续更新固定到发布者提供的新标签，重新添加市场并安装Lite；不要移动既有标签。回退也使用已验收的固定标签。安装包只包含Skill和公开连接信息，项目绑定、账号令牌和服务配置均不在此仓库。
