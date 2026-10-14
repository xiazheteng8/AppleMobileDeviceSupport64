# Apple iPhone 驱动组件下载与修复

解决 Microsoft Store 版 iTunes 导致部分第三方 iPhone 调试、侧载工具无法识别驱动的问题。

## 📺 关于频道

欢迎关注 YouTube 频道「折腾吧」，分享 iPhone、数码工具及技术折腾教程。

👉 [订阅「折腾吧」](https://www.youtube.com/@xiazheteng8)

## 问题说明

在 Windows 10 / Windows 11 上，部分用户通过 Microsoft Store 安装 iTunes 后，使用第三方 iPhone 调试、侧载或设备管理工具时，可能遇到以下问题：

- 提示 `iTunes not installed`
iTunes not installed — need Apple Mobile Device Support DLLs

- 提示缺少 `Apple Mobile Device Support`
- 提示找不到 Apple 驱动或相关 DLL
- iTunes 可以正常识别 iPhone，但第三方软件仍然提示驱动异常

这是因为部分第三方软件依赖 Apple Mobile Device Support 等组件，并通过特定的文件路径、注册信息或 DLL 检测 Apple 运行环境。由于 Microsoft Store 版与传统 Windows 安装版的安装机制和组件布局存在差异，部分第三方软件可能无法正确识别所需组件。

## 解决方案

本项目提供从 **Apple 官方 iTunes 安装包中提取的相关组件**，用于补充或修复第三方软件所需的 Apple 组件环境。

本项目中的组件来源于 Apple 官方软件安装包，并非第三方重新编译或修改的驱动。

### 📥 项目文件

| 文件 | 说明 |
|---|---|
| `AppleMobileDeviceSupport64` | Apple 移动设备支持组件，主要用于解决相关驱动及设备通信组件缺失的问题 |
| `Bonjour64` | Apple Bonjour 服务发现组件，部分软件可能需要 |
| `iTunes64` | iTunes 主程序安装组件 |

文件名及扩展名以仓库实际上传内容为准。

### 🛠️ 安装步骤

1. 下载本项目中的相关组件。
2. 解压下载的压缩包（如果有）。
3. 优先运行 `AppleMobileDeviceSupport64` 对应的安装程序，并根据提示完成安装。
4. 如果安装程序提示缺少依赖项，请根据提示补齐相关组件；不要强行跳过错误。
5. 安装完成后，重新启动电脑。
6. 重新连接 iPhone，打开原先提示驱动异常的第三方软件进行测试。

通常建议优先处理 Apple Mobile Device Support 相关组件。Bonjour 和 iTunes 主程序是否需要安装，应根据当前环境及第三方软件的具体依赖决定。

**注意：** 如果文件是 MSI 安装包，可以按安装程序提示操作；如果文件是普通 DLL、SYS 或 INF 文件，请勿直接复制到系统目录。组件安装方式应以实际文件类型为准。

## 适用场景

- 使用 Microsoft Store 版 iTunes 后，第三方软件提示未安装 iTunes。
- 第三方 iPhone 侧载工具无法检测 Apple Mobile Device Support。
- iTunes 能够识别 iPhone，但第三方工具提示驱动异常。
- 第三方软件提示缺少 Apple 相关 DLL
