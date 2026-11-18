# 🎓 TAR UMT Intranet Discord Bot (Bilingual / 中英双语)

[![Invite Bot](https://img.shields.io/badge/Discord-Invite%20Bot%20%2F%20%E9%82%80%E8%AF%B7%E6%9C%BA%E5%99%A8%E4%BA%BA-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/oauth2/authorize?client_id=1571890752328437780&permissions=18432&integration_type=0&scope=bot+applications.commands)

An automated, bilingual (English / 简体中文) Discord Bot built for TAR UMT students to check weekly timetables, track tuition bills, and receive proactive evening notifications directly in Discord DMs.

专为 TAR UMT（拉曼理工大学）学生打造的中英双语 Discord 机器人，支持直接在 Discord 内查询周课表、今日课程、学费账单，并提供每晚自动巡检与私信提醒功能。

---

## 🚀 Quick Start / 快速开始

1. **Invite the Bot / 邀请机器人:**  
   👉 **[Click here to invite TAR UMT Bot to your Discord Server / 点击此处将机器人邀请至你的 Discord 服务器](https://discord.com/oauth2/authorize?client_id=1571890752328437780&permissions=18432&integration_type=0&scope=bot+applications.commands)**
2. **Allow Direct Messages / 开启私信权限:**  
   Make sure you allow Direct Messages from server members in your Discord privacy settings so the Bot can send you automated evening reminders.  
   请确保在 Discord 隐私设置中允许“来自服务器成员的私信”，以便机器人每晚能顺利向你发送课程与账单提醒。
3. **Bind & Configure / 绑定与设置:**  
   Use `/bind` to link your student account, `/language` to choose English or 简体中文, and `/remind` to customize your alerts.  
   输入 `/bind` 绑定学生账号，使用 `/language` 切换中英文显示，并通过 `/remind` 自定义自动提醒开关。

---

## ✨ Features & Commands / 功能与指令介绍

All commands support ephemeral (private) responses so your personal academic and financial data are visible **only to you**.  
所有查询与设置指令均采用「仅自己可见（Ephemeral）」模式回复，确保你的课表和账单隐私不会在公共频道泄露。

| Command / 指令 | Description (EN) | 功能说明 (中文) |
| :--- | :--- | :--- |
| `/bind` | Bind your TAR UMT Student Intranet account via a secure popup modal. | 通过原生弹窗表单安全绑定你的 TAR UMT 学生内网账号。 |
| `/unbind` | Unlink your account and **permanently delete** all stored data from the database. | 解绑账号，并从云端数据库中**永久清除**你的所有数据。 |
| `/timetable` | View your current weekly class schedule, venues, lecturers, and replacement notes. | 查询本周完整课表（包含时间、地点、讲师及补课备注）。 |
| `/today` | Quickly check only today's classes and venues. | 快速查看仅限今天的课程安排与上课地点。 |
| `/billing` | Check your current tuition bills, amounts, and payment due dates. | 查询当前的学费账单明细、金额及缴费截止日期。 |
| `/remind` | Open an interactive control panel to toggle automated DM notifications on/off. | 打开交互式按钮面板，自由开关各项自动私信提醒。 |
| `/language` | Switch the Bot's display language between **English** and **简体中文**. | 切换机器人的显示语言（**English** / **简体中文**）。 |

### 🔔 Automated Evening Checks (22:00 MYT) / 每晚自动巡检规则
Every night at **22:00 (Malaysia Time, UTC+8)**, the Bot automatically checks your Intranet status if you have enabled reminders:  
每天晚上 **22:00（马来西亚时间 UTC+8）**，机器人会自动为开启了提醒的用户执行巡检：
- **Class Day Alert (休假后上课提醒):** Notifies you the night before if today is an off-day and tomorrow has scheduled classes. (若今天无课且明天有课，提前一晚通知你准备上课。)
- **Timetable Changes & Replacements (课表变更与补课提醒):** Alerts you when schedule changes are detected, and sends an advance notice the night before any replacement class. (检测到课表变动时通知，并在补课前一天晚上提前提醒。)
- **Billing Reminder (账单截止提醒):** Sends daily reminders once an unpaid bill is within **7 days** of its due date until paid. (当未缴账单距离截止日期 ≤ 7 天时，每晚提醒一次直到缴清。)

---

## ⚠️ Disclaimer & Terms of Use / 免责声明与使用须知

By using `/bind` and interacting with this Bot, you acknowledge and agree to the following terms:  
使用 `/bind` 绑定账号并使用本机器人，即表示你已阅读、理解并同意以下所有条款：

### 1. Do Not Rely Solely on This Bot / 请勿完全依赖本机器人
- This is an unofficial, student-built utility tool and is **not affiliated with or endorsed by TAR UMT**.  
  本工具为个人开发的非官方辅助机器人，**与 TAR UMT 官方没有任何关联或授权关系**。
- Due to potential university website maintenance, network fluctuations, server downtime, or Discord API limits, **timely delivery of reminders is NOT guaranteed**.  
  由于学校网站维护、网络波动、服务器停机或 Discord 接口限制等不可控因素，**本机器人无法保证所有提醒永远准时送达**。
- **Always check the official TAR UMT Student Intranet / TARCApp yourself.** If you miss a class, replacement session, or tuition payment deadline because you relied solely on this Bot, **the developer bears zero responsibility and will not be held liable.**  
  **请务必自行定期登录学校官方 Intranet 或 TARCApp 核对信息。** 若因过度依赖本机器人而导致错过上课、补课或学费缴纳截止日期，**开发者概不负责，请勿因此追究或联系开发者。**

### 2. Server Infrastructure & Latency / 服务器托管与延迟说明
- To keep this service free for students, the Bot runtime is hosted on free / budget third-party cloud hosting (located outside Malaysia). While the hosting provider is reputable, you may occasionally experience **slightly higher response latency (1–3 seconds)** or brief maintenance restarts.  
  为了向同学免费提供服务，本机器人的运行节点部署在海外的免费/高性价比云端服务器上（节点位于马来西亚外）。虽然托管商本身可信，但跨洲连接学校内网时可能会出现 **1～3 秒的轻微延迟**，或偶发性的节点维护重启。
- **Data Separation (存算分离架构):** Your credentials and academic data are **NOT stored on the hosting server's local disk**. All data is transmitted directly to and stored in an isolated cloud database (**Supabase**).  
  **数据与运行环境分离：** 你的账号密码及课表账单数据**绝不会保存在托管服务器的本地硬盘中**，所有数据均独立存储于受保护的云端数据库（**Supabase**）。

### 3. Security & Privacy / 隐私与数据安全声明
- Your Intranet password is **encrypted using symmetric encryption (Fernet / AES)** before being stored in Supabase, and is never logged in plain text. You can erase all your data at any time using `/unbind`.  
  你的学生内网密码在存入 Supabase 数据库前均经过 **高强度对称加密（Fernet / AES）** 处理，绝不以明文形式保存或打印在日志中。你随时可以使用 `/unbind` 指令一键彻底抹除所有个人数据。
- **Use at Your Own Risk:** If you have any doubts about the security of third-party tools, **please do not bind your account or use this Bot.**  
  **信任原则：** 如果你对第三方工具的安全性存在任何疑虑，**请勿绑定账号或使用本机器人。**
- While standard security practices are implemented, no online system is 100% immune to cyberattacks. In the unlikely event of a database breach or third-party infrastructure attack resulting in data leakage, **the developer cannot provide compensation or take legal/financial responsibility.**  
  尽管本系统已采取标准加密防护措施，但任何互联网服务都无法做到绝对的 100% 安全。若因极端情况（如第三方云平台遭受黑客攻击）导致数据泄露，**开发者无法对此承担任何赔偿或连带责任。**

### 4. Developer Pledge & Closed-Source Policy / 开发者承诺与闭源说明
- **Zero Snooping Commitment:** The developer personally pledges **never to inspect, access, or browse your personal account data, timetables, or billing details**. Only minimal operational logs (such as command execution status and sync success/failure timestamps) are collected to monitor Bot stability and troubleshoot errors.  
  **零窥探承诺：** 本人郑重承诺**绝不会去查看或翻阅任何用户的个人账号资料、课表或账单内容**。后台仅收集最基础的运行状态日志（如指令执行成功与否、巡检时间），用于确保机器人正常运行与排查故障。
- **Closed-Source Decision & Self-Hosting Requests:** The core source code of this project will **remain closed-source for the foreseeable future**. Because the developer cannot guarantee that every third party self-hosting this code would not modify it for malicious or illegal purposes (such as phishing or unauthorized scraping), keeping the source private is necessary to protect students and the university infrastructure. However, if you are genuinely interested in this project, have concerns about third-party data privacy, and wish to self-host it strictly for your own personal use, **you may contact me to request the source code — just please do not deceive me.**  
  **暂不开源说明与个人自部署申请：** 本项目的核心源码**暂时不会开源**。由于本人无法保证所有自行架设该代码的人都不会将其魔改用于非法用途（如搭建钓鱼机器人窃取密码或恶意攻击学校内网），为了保护同学与学校系统的安全，源码将保持私有。但如果你对这个项目确实感兴趣，同时担心个人资料安全、希望自己架设供个人使用，**可以联系我获取源代码，但请不要欺骗我。**

### 5. Feature Scope & Future Suggestions / 功能边界与建议反馈
- **Sufficient as a Reminder Tool:** The current feature set is intentionally focused on daily schedule and billing reminders, which is already sufficient for its intended purpose. **Features involving critical applications, exam timetables/results, or sensitive personal actions will not be considered** — nobody should rely on a third-party Bot for high-stakes academic matters.  
  **功能定位说明：** 目前的功能作为一款日常提醒机器人已经足够使用。**涉及重要申请、考试时间/成绩查询或各类触及高度个人隐私的操作将不会考虑加入**——这种关乎学业的大事，本就不应该依赖第三方机器人来处理。
- **No Auto-Attendance:** Automated attendance check-in is technically near-impossible as it requires being connected to the campus network, and **even if it were possible, I will never build it.** If you are looking for an auto-attendance tool, you might want to consider dropping out instead.  
  **关于自动点名：** 自动点名在技术上几乎不可能实现（需要连接校园内网验证），而且**就算能做到我也不会做**。如果你需要这个功能，不如考虑退学吧。
- **Feature Suggestions Welcome:** If you think there are other **reasonable and practical features** that would fit this Bot well, feel free to suggest them — I will definitely consider adding them!  
  **欢迎提出建议：** 如果你认为有什么其他**合理且实用**的功能适合加入这个机器人，欢迎随时向我建议，我会认真考虑的。
