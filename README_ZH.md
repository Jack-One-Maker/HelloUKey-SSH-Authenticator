[English](README.md) | [简体中文](README_ZH.md)
<p align="center">
  <a href="https://apps.microsoft.com/detail/9n0wbprdgf78?referrer=appbadge&cid=GitHub&mode=full" target="_blank">
    <img src="https://store-images.s-microsoft.com/image/apps.10175.13912981154273113.82a12b87-2a83-4e8f-907f-b3bc680f02b6.0060320e-244d-42df-b211-b84193e28e57?h=170" width="150" alt="项目 LOGO">
  </a>
</p>

<h1 align="center">HelloUKey - SSH Authenticator</h1>
<p align="center">使用 TPM 和 Windows Hello 保护 SSH 密钥，通过指纹、人脸识别或PIN码实现安全的 SSH 登录认证</p>

## 摘要
一款 Windows 原生 SSH 安全认证应用，基于电脑自带的 TPM 芯片和 Windows Hello 保护 SSH 私钥不受攻击和窃取。应用生成可直接使用的 Windows Hello 密钥以实现通过指纹或人脸识别来实现 SSH 免密安全认证。

## 下载链接
<a href="https://apps.microsoft.com/detail/9n0wbprdgf78?referrer=appbadge&cid=GitHub&mode=full" target="_blank"  rel="noopener noreferrer">
	<img src="https://get.microsoft.com/images/zh-cn%20dark.svg" width="200"/>
</a>

## 应用截图
![图片描述](https://store-images.s-microsoft.com/image/apps.27420.13912981154273113.82a12b87-2a83-4e8f-907f-b3bc680f02b6.cfa3c166-85d1-44dd-878d-ebc447c3debe)

![图片描述](https://store-images.s-microsoft.com/image/apps.64475.13912981154273113.82a12b87-2a83-4e8f-907f-b3bc680f02b6.a14a7ddd-d147-4d2d-9917-2b429eaa72c3)

## 功能及特性
🔐 快速创建与生成受硬件保护的 SSH 安全密钥，排除 SSH 私钥在硬盘上存放时被盗取的风险；<br>

🔐 使用 Windows Hello 生物特征识别免密登录 SSH Server;<br>

🔐 私钥完全从硬件生成且永远无法导出，不接受导入外部密钥（外部密钥无法保证安全性）；<br>

🔐 适用于运维、开发人员、网络工程师等人员的提效安全利器；<br>

🔐 适配 OpenSSH、Git、WinSCP、PuTTY、SecureCRT、MobaXterm等的安全认证<br>

🔐 支持 Win11 效能模式，最小化运行时以低功耗、低优先级进程模式运行，平板使用更节能；<br>

🔐 支持设置开机自动启动；<br>

🔐 单机应用，不上传或同步任何数据，全面保障隐私；<br>

🔐 原生 WinUI 应用，非网页包装，运行更节省资源；<br>

🔐 Microsoft Store 打包应用，经微软签名认证的安全应用；<br>

🔐 仅十几 MB 的小尺寸安装包，节省硬盘空间；<br>


## 操作系统
💽 Windows 10 1903（内部版本18362.0）及更高版本

## 常见问题 - FAQ

- Q: 使用这款应用时是否需要额外购买 USB 硬件密钥？<br>
  A: 不需要，HelloUKey 基于电脑自带的 TPM硬件生成并管理密钥，它是作为 SSH Agent 存在的一个认证器。<br>

- Q: 是否支持从外部导入私钥？<br>
  A: 目前仅支持直接从基于 TPM 的 Windows Hello 生成 SSH 密钥并提供硬件级别的安全认证，不排除在未来的计划中加入导入功能。<br>

- Q: 在 Windows 上使用 PuTTY 或 WinSCP，可以用 HelloUKey 替代 Pageant 实现免密登录吗？<br>
  A: 是的，它同时作为 OpenSSH 代理与 Pageant 代理，因此它支持 WinSCP等以 Pageant 作为代理的客户端。<br>

- Q: 为什么登录 SSH 时弹出的是PIN码输入窗口，而别人电脑出现的是指纹和人脸识别弹窗？<br>
  A: 因为指纹识别需要指纹识别器并配置 Windows Hello，除了电脑自带的指纹识别器，您也可以外接支持 Windows Hello 的指纹识别器。<br>

- Q: 应用是否支持在 Surface 等 Windows 平板上使用？<br>
  A: 非常适合在此类设备上使用，它支持原生 x64、x86 与 Arm64 三种处理器架构，只要满足操作系统版本大于等于 Win10 1903(18362) 即可安装使用。<br>

- Q: 是否可以将一个 HelloUKey 密钥用于多个服务端？<br>
  A: 完全可以使用同一个私钥来管理你的 Server 或设备的登录认证。<br>

- Q: 应用是否适用于 Git代码仓库的 SSH 认证？<br>
  A: 非常适合，Git 在 Windows 中使用 OpenSSH 的 ssh 工具，它支持直接与代理交互完成认证。**[使用 HelloUKey 生成 GitHub 认证密钥](./docs/github-config.md)**<br>

- Q: 应用都支持哪些 SSH 服务端的认证？<br>
  A: 理论上所有支持 SSH Server 的服务器、网络设备、终端等均支持，仅需要将公钥配置到服务端即可。<br>

## 更多文档
**[相关文档](./docs/README.md)**
