# ReTime 隐私政策 / Privacy Policy

生效日期 / Effective date：2026-11-05
适用产品：ReTime for iPhone / iPad（App Store 版，版本 1.6.2）
开发者：Feng Qiu（独立开发者）

---

## 中文

### 一句话

**ReTime 不收集你的数据。** 你的记录保存在你自己的设备上；除非你主动配置备份通道，否则不会离开设备。

### 我们不做什么

- 没有账号、没有注册、没有登录。
- 没有广告 SDK、没有分析 SDK、没有崩溃上报、没有遥测、没有第三方追踪。
- 我们不运营接收用户数据的服务器，也没有这样的服务端。
- App 启动时不联网；没有后台上传，没有版本检查请求。

### 数据存在哪里

- 你的内容（事项、日程、日记、备忘录、记账、生理期、倒数日、速记、剪贴板历史等）以标准 SQLite 数据库文件保存在本机 App 数据目录。
- 设置与偏好保存在本机 `UserDefaults`，只供本 App 读取。
- 模块密码锁是**界面门禁，不是磁盘加密**；口令以哈希形式保存在本机，数据库文件本身是明文，方便你随时用自己的工具打开。
- 你可以在「设置 → 数据 → 数据位置」查看数据库路径，在「设置 → 备份 → 备份恢复」导出整库备份包。

### 唯一会联网的情况（由你主动开启）

1. **WebDAV 备份**：只有当你在「设置 → 备份 → 备份通道」填入自己的 WebDAV 服务器地址与凭据后，App 才会把备份数据发送到**你指定的那台服务器**。凭据用 AES-GCM 加密后保存在本机。
2. **本机文件夹备份**：写入你通过系统文件选择器授权的目录。如果该目录本身是某个同步盘，后续同步由那个同步盘自行完成，我们不参与、也看不到。

除此之外没有任何网络请求。

### 系统权限与用途

| 权限 | 用途 | 数据去向 |
| --- | --- | --- |
| 通知 | 到点提醒，由系统通知中心投递本地通知 | 不离开设备 |
| 日历（只读） | 把系统日历里的会议、节假日订阅叠加到日程 | 不离开设备 |
| 相册 / 相机 | 选择或拍摄照片，插入日记与备忘录 | 只写入本机数据库 |
| 本地网络 | 连接同一局域网内的 WebDAV / NAS 备份服务器 | 发往你指定的服务器 |

所有权限都可以在 iOS「设置 → ReTime」里随时关闭；关闭后对应功能停用，不影响其他功能。

### 儿童

ReTime 不面向 13 岁以下儿童，也不会有意收集儿童数据。

### 删除与导出

卸载 App 会删除本机数据库。你可以先导出备份包再卸载；备份包由你自己保管，我们无法访问、也无法代为删除。恢复备份是整库覆盖，会替换当前数据，请在确认前自行核对。

### 联系我们

隐私相关问题：windcool99@agent.qq.com
或在公开仓库提交 Issue：https://github.com/windcool18-maker/ReTime-releases/issues

### 变更

政策变更会更新本页并修改顶部生效日期。

---

## English

**ReTime does not collect your data.** Everything you write stays on your device unless you explicitly set up a backup destination of your own choosing.

- **No account, no sign-in.** There is no user account system of any kind.
- **No tracking, no analytics, no ads.** The app contains no third-party SDK, no crash reporter, no telemetry, and no advertising identifier usage. We operate no server that receives user data.
- **No network access at launch.** The app makes no network request on startup and has no version-check call.
- **Local storage.** Your entries are stored in a standard SQLite database inside the app's data container; preferences live in `UserDefaults` and are readable only by this app. The optional module passcode is a UI gate, not disk encryption — the passcode is stored as a hash locally and the database remains readable with your own tools.
- **The only network traffic is user-initiated backup.** If you configure a WebDAV server in Settings → Backup, the app sends the backup archive **to the server you specified**; credentials are stored locally encrypted with AES-GCM. If you choose a local folder via the system file picker, the archive is written there (any sync is performed by that folder's own sync service, not by us).
- **Permissions.** Notifications (local, delivered by the system), Calendar (read-only overlay), Photos / Camera (insert images into entries), and Local Network (reach a WebDAV / NAS server on your LAN). All can be revoked in iOS Settings at any time.
- **Children.** ReTime is not directed at children under 13 and does not knowingly collect data from them.
- **Deletion.** Uninstalling the app removes the local database. You can export a full backup first; backups are yours to keep and we cannot access or delete them.

Privacy questions: windcool99@agent.qq.com
Issues: https://github.com/windcool18-maker/ReTime-releases/issues

Changes to this policy are reflected on this page with an updated effective date.
