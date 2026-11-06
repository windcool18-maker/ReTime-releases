# ReTime 技术支持 / Support

适用产品：ReTime for iPhone / iPad（App Store 版）
开发者：windcool99（独立开发者）
系统要求：iOS 17.0 / iPadOS 17.0 或更高
当前版本：1.6.2

---

## 开始使用

打开 App 就能直接记录，不需要注册、登录或任何激活步骤。所有模块一开始就是可用的。

App 第一次打开是空的，这是正常的。想先看看界面长什么样，可以：
**设置 → 数据 → 示例数据 → 载入示例数据**（示例文字带「[样例]」前缀，随时可点「清除示例数据」）。
已经有自己记录的模块不会被示例改动。

## 常见问题

**我的数据存在哪里？**
存在这台设备上的 App 数据目录，是标准 SQLite 数据库文件。可以在「设置 → 数据 → 数据位置」查看路径。开发者没有服务器，也收不到你的数据。

**怎么备份？**
「设置 → 备份」分三块：备份通道（选本机文件夹或 WebDAV）、备份策略（立即备份 / 自动备份）、备份恢复（导出备份包 / 从备份恢复 / 合并备份）。
备份包是一个文件夹，请整个文件夹一起保管。「合并备份（不动本地数据）…」只增不减；「从备份恢复…」是整库覆盖，会替换当前数据，操作前请确认选的是最新的那一版。

**换设备怎么搬？**
旧设备导出备份包 → 整个文件夹搬到新设备 → 新设备「设置 → 备份 → 备份恢复 → 从备份恢复…」。恢复后 App 会重新载入数据，不需要卸载重装。模块密码锁不随备份迁移，需要在新设备重新设置。

**备份会自动同步吗？**
不会。没有自动双向同步，备份包交换也不等于多端同步。跨设备靠你自己导出 / 恢复，恢复是整库覆盖。

**WebDAV 连不上？**
- 确认服务器地址带尾斜杠，且能从这台设备访问；
- 局域网内的 NAS / 自建服务器，首次访问时系统会询问「本地网络」权限，请允许；公网服务器建议使用 https；
- 坚果云等服务要用「应用密码」，不是登录密码；
- 在「设置 → 备份 → 备份通道」里点测试连接，看到「目标已就绪」后，「立即备份」才会可用。

**提醒到点不响？**
提醒由 iOS 系统通知中心投递，不依赖 App 常驻。请确认「设置 → 通知」里允许了 ReTime 的通知，且事项上确实勾了提醒并设了提前量。App 在前台时也会显示提醒。

**日程里看不到系统日历的会议？**
「设置 → 通用 → 日程 · 系统日历」打开开关并允许日历访问。这是只读叠加，App 绝不会新增、修改或删除你的日历事件。

**怎么更新？**
通过 App Store 更新。更新不会覆盖或上传你记录的数据。

**日记 / 备忘录的富文本会丢吗？**
正文用标准 RTFD 存储，随备份包一起带走。表格与引用块在 iOS 上以制表位 / 缩进呈现，与桌面端排版可能略有差异。

## 联系我们

- 邮箱：windcool99@agent.qq.com
- Issue：https://github.com/windcool18-maker/ReTime-releases/issues

个人项目，回复可能不及时，但每一条都会看。报问题请带上：**iOS / iPadOS 版本、ReTime 版本、复现步骤**，能附截图更好。

---

## Support (English)

ReTime works offline and needs no account. Your data is stored in a local SQLite database on the device; the developer operates no server that receives it.

- First launch is empty by design. To preview the UI: **Settings → Data → Sample Data → Load Sample Data** (entries are marked `[Sample]` and can be cleared).
- Backups: **Settings → Backup**. Choose a local folder or your own WebDAV server, then export a backup package. Restoring replaces the whole database; merging only adds records.
- There is no automatic two-way sync. Moving data across devices is a manual export / restore.
- Reminders are local notifications delivered by iOS; the app does not need to stay running.
- Calendar access is read-only and optional.
- Updates are delivered through the App Store.

Contact: windcool99@agent.qq.com · Issues: https://github.com/windcool18-maker/ReTime-releases/issues
