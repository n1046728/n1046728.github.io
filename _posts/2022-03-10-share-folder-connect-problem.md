---
title: Share folder can't access after ad password changed
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-10 16:53:55 +0800
categories: []
tags: [windows]     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
This occur I enter remote windows server using local account and share folder using ad account.After I change ad password then I can't access share forder.This article will tell u how to solve it.
<!--more-->
## cause and solve
> Network table keep your previous connection information ,so u can use command **net use /delete**.It will clear connection info.
> You reaccess share folder will show Window Security window and enter account/new password.

```console
> net use

Status        Local       Remote                 Network
--------------------------------------------------------------------------
ok                        \\tp123\IPC$    Microsoft Windows Network

> net use * /delete 
```

## reference 
* [How to restore access to a windows shared folder after host password change? - **stackoverflow ozzylee**](https://stackoverflow.com/questions/54898305/how-to-restore-access-to-a-windows-shared-folder-after-host-password-change)
* [How to delete cached temporarily credentials for a network share on a Windows machine without rebooting or logging off - **serverfault**](https://serverfault.com/questions/451387/how-to-delete-cached-temporarily-credentials-for-a-network-share-on-a-windows-ma)
* [Windows Credential Manager - **Window OSHub**](http://woshub.com/saved-passwords-windows-credential-manager/)
