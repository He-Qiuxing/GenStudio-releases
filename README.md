# GenStudio

**GenStudio** 是一款面向 Windows 的 **AIGC 图片创作桌面应用**。
把 AI 生图、参数调试、历史管理、本地工作区整理放在同一个界面里，适合日常创作与批量出图。

> 本仓库是 **官方发布仓库**，用于托管 Windows 安装包与自动更新文件。
> 这里 **不存放源码**，只发布可安装的正式版本。

---

## 这是什么

GenStudio 面向需要稳定本地桌面体验的创作者：

- 用图形界面调用 AI 生图接口
- 管理提示词、模型通道、参考图
- 查看任务队列与生成结果
- 保存历史记录、评分与本地工作区图片
- 通过 GitHub Releases 自动检查与安装更新

适合：

- 个人创作者 / 设计师
- 需要本地长期保存作品的用户
- 希望一键安装、开机即用的 Windows 用户

---

## 主要能力

### 创作
- 多模型 / 多通道 API 配置
- 提示词润色
- 参考图与局部编辑相关能力
- 任务队列与结果面板

### 本地管理
- 历史记录落盘保存
- 图片评分
- 折叠工作区 / 外部文件夹浏览
- 本地图片导出与整理

### 桌面体验
- Windows 安装包（NSIS）
- 启动后自动检查更新
- 设置页可手动「检查更新」
- 用户数据与安装目录分离，更新后尽量保留配置与历史

---

## 下载安装

### 最新版本

**[下载最新安装包（Releases）](https://github.com/hejunrui63-sketch/GenStudio-releases/releases/latest)**

当前正式版文件名通常为：

```text
GenStudio-Setup-x.y.z.exe
```

例如：`GenStudio-Setup-1.0.2.exe`

### 安装步骤

1. 打开 [Releases](https://github.com/hejunrui63-sketch/GenStudio-releases/releases)
2. 下载最新的 `GenStudio-Setup-*.exe`
3. 双击安装
4. 安装完成后从开始菜单或桌面快捷方式启动

### Windows 安全提示（重要）

当前安装包 **未做代码签名**。
首次安装时，Windows SmartScreen 可能会提示「未知发布者」：

1. 点击 **更多信息**
2. 再点 **仍要运行**

这是未签名软件的常见情况，不是安装包损坏。

---

## 自动更新

GenStudio 内置基于 **GitHub Releases** 的自动更新：

1. 启动后静默检查是否有新版本
2. 发现更新后后台下载
3. 下载完成后提示重启安装
4. 也可在设置页手动点击「检查更新」

更新源就是本仓库：

```text
hejunrui63-sketch/GenStudio-releases
```

---

## 本仓库里有什么

每个版本的 Release 通常包含：

| 文件 | 作用 |
|------|------|
| `GenStudio-Setup-x.y.z.exe` | Windows 安装包 |
| `GenStudio-Setup-x.y.z.exe.blockmap` | 差分更新辅助文件 |
| `latest.yml` | 自动更新元数据（版本号、校验值等） |

说明：

- 普通用户只需要下载 `.exe` 安装包
- `latest.yml` 与 `.blockmap` 主要给客户端自动更新使用

---

## 系统要求

- 操作系统：Windows 10 / 11（64 位）
- 网络：首次配置 API、检查更新时需要联网
- 磁盘：建议预留足够空间存放生成图片与历史数据

用户数据默认保存在 Electron `userData` 目录，卸载时通常不会自动删除你的历史与配置。

---

## 使用前准备

1. 安装并打开 GenStudio
2. 在 API 配置中填写你自己的模型服务地址与密钥
3. 开始生成图片
4. 可在设置中配置历史清理策略、检查更新等

> 本软件本身不附带第三方模型密钥。
> API Key 请自行向对应服务商申请，并注意保密。

---

## 版本发布说明

- 版本号遵循语义化版本：`主版本.次版本.修订号`，例如 `1.0.2`
- 每个正式版都会发布到本仓库的 [Releases](https://github.com/hejunrui63-sketch/GenStudio-releases/releases)
- 发布后客户端即可通过自动更新检测到新版本

查看全部历史版本：
https://github.com/hejunrui63-sketch/GenStudio-releases/releases

---

## 常见问题

### 1. 为什么安装时提示未知应用？
因为安装包尚未代码签名。选择「更多信息 → 仍要运行」即可。

### 2. 更新后历史记录还在吗？
正常情况下会保留。程序更新主要替换软件本体，用户数据目录中的配置、历史与图片会尽量保留。

### 3. 这个仓库为什么没有源码？
这是 **发布仓库**，只用于安装包分发和自动更新。
不是源码仓库。

### 4. 我只想手动安装，不自动更新可以吗？
可以。直接下载 Releases 里的安装包手动安装即可。
即使开启检查更新，也只有在你确认安装时才会完成升级。

---

## 项目定位一句话

**GenStudio = Windows 本地 AIGC 创作桌面端 + GitHub 自动更新发布通道。**

---

## 链接

- 最新下载：https://github.com/hejunrui63-sketch/GenStudio-releases/releases/latest
- 全部版本：https://github.com/hejunrui63-sketch/GenStudio-releases/releases
- 仓库主页：https://github.com/hejunrui63-sketch/GenStudio-releases

---

## 免责声明

- 请遵守你所使用 AI 服务商的服务条款与当地法律法规
- 请自行妥善保管 API 密钥，不要把密钥提交到公开位置
- 软件按现状提供；使用前请自行评估数据备份与安全策略