# How can I perform SSH authentication more securely on Windows?

### I. Security Risks of Traditional Keys
As a programmer, operations specialist, or network engineer, you may log in via SSH dozens of times a day to various production servers, network devices, test environments, or hosted repositories.

For convenience, the common practice is to use the `ssh-keygen` command-line tool to generate a public-private key pair in the `user.ssh` directory. Taking RSA keys as an example, the public key is the `id_rsa.pub` file, and the private key is the `id_rsa` file.

When using this setup, the contents of the public key file (`id_rsa.pub`) are simply copied to the SSH server to enable password-less SSH login.

However, this approach directly exposes the private key file `id_rsa` to Windows user-level security permissions, meaning that any software or program running under the current user can silently and legitimately read and upload the private key file. In complex modern network environments, the vulnerability of private keys stored on hard drives is as thin as a sheet of paper.

Some users, in an effort to ensure security, set complex passwords for their private keys. Entering a password to unlock the private key before every login not only reduces efficiency but also makes it extremely easy to forget passwords if they differ across multiple servers.


Others, in pursuit of completely password-less login, simply choose not to set a password for their private key, resulting in a seamless experience.


To address these complex security issues, many enterprises explicitly require the use of hardware keys or custom security keys for authentication and prohibit the storage of private keys on local hard drives.


### II. The Cornerstone of Modern Security Keys: Hardware Isolation and the Challenge Mechanism
Traditional key authentication mechanism: The private key on the hard drive is read into memory to complete a digital signature for the challenge.


Hardware Key Authentication Mechanism: The challenge is sent to the hardware, where the digital signature is completed within the secure chip and returned.


As can be seen, the hardware-isolated authentication mechanism provides significant protection against private key theft. The private key is never read into memory, and plaintext is never exposed outside the isolated chip; data is signed within the secure chip only when necessary. Additionally, most hardware USB keys require the user to provide confirmation directly on the USB key.


However, such USB keys have their own drawbacks: first, they are relatively expensive; second, they must be carried at all times, otherwise work cannot be performed. So, is there a perfect solution that offers hardware-level security while being cost-free and impossible to lose or misplace?


### III. TPM Chip – The Computer’s Built-in Hardware Key Chip
The vast majority of PCs we use today already contain a TPM (Trusted Platform Module). Some are dedicated chips soldered onto the motherboard, while others are emulated chips (fTPM) embedded in the CPU firmware. Although these two forms differ in implementation, they both serve as hardware-isolated security devices. The difference in security between them is not significant, as scenarios where someone would disassemble a computer to crack the system are extremely rare. As always, there is no such thing as absolute security, but we can achieve a relatively high level of security.


Therefore, we can directly leverage the TPM’s hardware security level to ensure the security of SSH keys. Combined with Windows Hello for in-person authentication via fingerprint, facial recognition, or PIN, this allows for a very convenient and fast SSH login.


HelloUKey is a native modern Windows application that uses TPM 2.0 and Windows Hello to provide secure and convenient SSH proxy authentication. It supports secure authentication for common clients such as OpenSSH, Git, WinSCP, and PuTTY. As a standalone application, it ensures privacy and security.


HelloUKey is extremely user-friendly. When generating keys, it automatically isolates and protects SSH keys within the TPM and manages the resulting key configurations. It supports initiating connections directly in the terminal using the "ssh [key name]" command, which triggers a Windows Hello authentication prompt.


HelloUKey’s feature API set and security have been certified by the Microsoft Store, and every released version is digitally signed in compliance with Microsoft standards. As long as you install it through official channels, you need not worry about malicious calls or permission abuse. We recommend that interested users click the link below to install it:

<a href="https://apps.microsoft.com/detail/9n0wbprdgf78?referrer=appbadge&cid=GitHubEN&mode=full" target="_blank"  rel="noopener noreferrer">
	<img src="https://get.microsoft.com/images/en-us%20dark.svg" width="200"/>
</a>
