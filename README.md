# SeanSu · 自动更新发布通道

这个仓库**只放安装包**，不放源码。

SeanSu（账号管理器）里的「检查更新」读的就是这个仓库的 Release 接口：
`https://api.github.com/repos/1235555lk-gif/seansu-release/releases/latest`

## 怎么装

到 [最新版](https://github.com/1235555lk-gif/seansu-release/releases/latest) 下载
`SeanSu-Setup-<版本>.exe`，双击安装即可。
装过一次之后，打开「设置 → 外观与版本 → 检查更新」就能查到后续版本。

## 每个 Release 里有什么

| 文件 | 用途 |
|---|---|
| `SeanSu-Setup-<版本>.exe` | 安装包本体（客户端下载的就是它） |
| `SHA256SUMS.txt` | 安装包的 sha256（客户端下完照它核对；走加速代理时尤其有用） |

## 关于自动更新

- 客户端只**读**这个仓库，不需要任何令牌，也不需要在谁的机器上起任何服务。
- 程序**不会自己偷偷升级**：检查是你点的，下载是你点的，安装也是你点的。
- 程序里没有任何上传 / 发布代码；往这个仓库发版本是人工跑一条命令
  （`_publish*.py --go`），什么时候发由人拍板。

## 加速（可选）

国内直连 `api.github.com` 一般能通。真不通时，在设置里把「加速前缀」填成
`https://gh-proxy.com` —— 它同时能代理查询接口和安装包下载。
（`https://ghfast.top` 只能代理下载，代理查询接口会回 403。）
