```
要获取Git签名密钥ID，可以通过以下步骤进行操作：

1. **检查已有的SSH密钥**：在您的计算机上打开终端或命令提示符，输入`ls -al ~/.ssh`来查看是否已经存在SSH密钥文件（通常是`id_rsa.pub`）。
2. **生成新的SSH密钥**：如果您还没有SSH密钥，可以使用`ssh-keygen`命令来生成。在终端中输入`ssh-keygen -t rsa -C "your_email@example.com"`，将其中的电子邮件地址替换为您的实际邮箱地址。按回车键接受默认的文件位置和名称。
3. **复制SSH公钥内容**：使用`cat ~/.ssh/id_rsa.pub`命令来查看并复制您的SSH公钥内容。这个长字符串就是您的SSH密钥ID。
4. **添加SSH密钥到GitHub**：登录到您的GitHub账户，点击右上角的头像，选择“Settings”选项。在左侧菜单中选择“SSH and GPG keys”，然后点击“New SSH key”。给您的SSH密钥起一个名字，粘贴您复制的公钥内容到“Key”字段中，最后点击“Add SSH key”。
5. **验证SSH密钥**：添加完成后，您可以使用`ssh -T git@github.com`命令来测试SSH连接是否成功。如果看到“Hi ! You've successfully authenticated, but GitHub does not provide shell access.”，则表示SSH密钥已经成功添加到您的GitHub账户。
```

TortoiseGit 提示 No supported authentication methods available 错误
```
进入小乌龟设置
选择网络面板
设置ssh客户端为git客户端（客户端位置=.\Git\usr\bin\ssh.exe

```