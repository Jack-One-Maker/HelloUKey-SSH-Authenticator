[English](README.md) | [简体中文](README_ZH.md)
<p align="center">
  <a href="https://apps.microsoft.com/detail/9n0wbprdgf78?referrer=appbadge&cid=GitHub&mode=full" target="_blank">
    <img src="https://store-images.s-microsoft.com/image/apps.10175.13912981154273113.82a12b87-2a83-4e8f-907f-b3bc680f02b6.0060320e-244d-42df-b211-b84193e28e57?h=170" width="150" alt="项目 LOGO">
  </a>
</p>

<h1 align="center">HelloUKey - SSH Authenticator</h1>
<p align="center">Protect your SSH keys using TPM and Windows Hello to enable secure SSH login authentication via fingerprint, facial recognition, or PIN.</p>

## Abstract
A native Windows SSH security authentication app that leverages the computer’s built-in TPM chip and Windows Hello to protect SSH private keys from attacks and theft. The app generates ready-to-use Windows Hello keys to enable password-free SSH authentication via fingerprint or facial recognition.

## Download
<a href="https://apps.microsoft.com/detail/9n0wbprdgf78?referrer=appbadge&cid=GitHubEN&mode=full" target="_blank"  rel="noopener noreferrer">
	<img src="https://get.microsoft.com/images/en-us%20dark.svg" width="200"/>
</a>

## Screenshots
![image0](https://store-images.s-microsoft.com/image/apps.8377.13912981154273113.82a12b87-2a83-4e8f-907f-b3bc680f02b6.c8aa1c3d-ae7c-4537-88ee-4c64834d24ba)

![image1](https://store-images.s-microsoft.com/image/apps.33150.13912981154273113.82a12b87-2a83-4e8f-907f-b3bc680f02b6.9f673b1c-850e-4399-9495-e7aeb9e0f6eb)

## Features and Specifications
🔐 Quickly create and generate hardware-protected SSH security keys, eliminating the risk of SSH private keys being stolen when stored on a hard drive. <br>

🔐 Use Windows Hello biometrics for password-less login to an SSH server. <br>

🔐 Private keys are generated entirely by the hardware and can never be exported; external keys cannot be imported (as their security cannot be guaranteed). <br>

🔐 A powerful tool for improving efficiency and security, designed for operations and maintenance staff, developers, network engineers, and others. <br>

🔐 Supports security authentication for OpenSSH, Git, WinSCP, PuTTY, SecureCRT, MobaXterm, and others. <br>

🔐 Supports Windows 11 Performance Mode; when minimized, it runs in low-power, low-priority process mode for more energy-efficient tablet use. <br>

🔐 Supports automatic startup at boot. <br>

🔐 A standalone app that does not upload or sync any data, ensuring complete privacy. <br>

🔐 Native WinUI app, not a web app wrapped in a native shell, so it runs more efficiently. <br>

🔐 Apps packaged by the Microsoft Store; secure apps signed and certified by Microsoft. <br>

🔐 A small installation package of just a few dozen MB, saving hard drive space. <br>


## Operating System
💽 Windows 10 version 1903 (18362.0) and later

## FAQ


- Q: Do I need to purchase an additional USB hardware key to use this app?<br>
A: No, HelloUKey generates and manages keys using your computer’s built-in TPM hardware; it functions as an authenticator that acts as an SSH agent.<br>


- Q: Does it support importing private keys from external sources?<br>
A: Currently, it only supports generating SSH keys directly from TPM-based Windows Hello and provides hardware-level security authentication. We do not rule out adding an import feature in future updates.<br>


- Q: When using PuTTY or WinSCP on Windows, can I use HelloUKey to replace Pageant for password-less login?<br>
A: Yes, it functions as both an OpenSSH agent and a Pageant agent, so it supports clients like WinSCP that use Pageant as their agent. <br>


- Q: Why does a PIN entry window pop up when I log in to SSH, while others see fingerprint and facial recognition prompts on their computers? <br>
A: Because fingerprint recognition requires a fingerprint reader and Windows Hello configuration. In addition to the computer’s built-in fingerprint reader, you can also connect an external fingerprint reader that supports Windows Hello. <br>


- Q: Does the app support use on Windows tablets such as the Surface? <br>
A: It is ideal for use on such devices. It supports the three native processor architectures: x64, x86, and Arm64. As long as the operating system version is Windows 10 1903 (18362) or later, you can install and use it. <br>


- Q: Can a single HelloUKey key be used for multiple servers? <br>
A: You can certainly use the same private key to manage login authentication for your servers or devices. <br>


- Q: Is the app suitable for SSH authentication with Git code repositories? <br>
A: It’s ideal. Git uses the OpenSSH ssh tool on Windows, which supports direct interaction with proxies to complete authentication. **[Generating GitHub Authentication Keys with HelloUKey](./docs/github-config.md)**<br>


- Q: Which SSH servers does the application support for authentication?<br>
A: In theory, it supports all servers, network devices, terminals, and other systems that support SSH servers; you simply need to configure the public key on the server.<br>

## Documents
**[Related Documents](./docs/README.md)**
