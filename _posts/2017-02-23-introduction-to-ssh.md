---
layout: post
title: SSH and it's use in GitHub
---

> "Privacy is Security, Security is Victory"

# What is SSH
**Secure Shell (SSH)** is a [cryptographic network protocol](https://en.wikipedia.org/wiki/Secure_Shell) for operating network services securely over an unsecured network.
SSH provides a secure channel over an unsecured network in a client-server architecture, connecting an SSH client application with an SSH server. Common applications include remote command-line login and remote command execution, but any network service can be secured with SSH.

# How does it works
To use a manually generated public-private key pair to perform the authentication, allowing users or programs to log in without having to specify a password. In this scenario, anyone can produce a matching pair of different keys (public and private). The public key is placed on all computers that must allow access to the owner of the matching private key (the owner keeps the private key secret). While authentication is based on the private key, the key itself is never transferred through the network during authentication. SSH only verifies whether the same person offering the public key also owns the matching private key. In all versions of SSH it is important to verify unknown public keys, i.e. associate the public keys with identities, before accepting them as valid. Accepting an attacker's public key without validation will authorize an unauthorized attacker as a valid user.

![copy](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Ssh_binary_packet_alt.svg/250px-Ssh_binary_packet_alt.svg.png)

# How to use
* Linux has native support for SSH, while Windows doesn't. <sup>[Ref](http://arstechnica.com/information-technology/2015/06/microsoft-bringing-ssh-to-windows-and-powershell/)</sup>
* Git Bash by default contains SSH package.<sup>[Download](https://git-for-windows.github.io/)</sup>
* Navigate to
  * `user/.ssh/` in Windows
  * `home/.ssh/` in Linux
  
  to list all the key-pair present in your machine. Only the file named **`id_rsa`** will be considered in *bash*
* Every key has a public counter-part, filename ending with **`.pub`**.

### How to create a new key
```
$ ssh-keygen -t rsa -C "your_email@example.com"
```
The file will be stored in afforesaid directory along with the fingerprint.
![copy](https://confluence.atlassian.com/bitbucketserver/files/776639788/776639789/1/1386202193726/STASH_11_win_keygen_1.png)
![copy](https://confluence.atlassian.com/bitbucketserver/files/776639788/776639790/1/1386202193276/STASH_11_win_keygen_2.png)

#### Note: The key-pair will create effect only if both of them are renamed as `id_rsa` and `id_rsa.pub` respectively.

### How to deploy keys in GitHub
* Copy the content of the file **id_rsa.pub**
* Move to the **Settings** option in right-top corner of the page
* In the user settings sidebar, click **SSH and GPG keys**.
* Click **New SSH key** or **Add SSH key**.
* Specify the **Title** according to your machine/workspace and paste the content in **Key** field.
* Click **Add SSH key**.
* If prompted, confirm your GitHub password.

#### [For more details, navigate here](https://help.github.com/articles/connecting-to-github-with-ssh/)

### Happy Coding! :)
