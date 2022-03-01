---
title: How to get details about a process in windows
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-01 09:50:05 +0800
categories: [windows, power shell]
tags: [power shell]     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
Memo how to get details about process
<!--more-->

## get process info
1. open task manager
2. select tab detail 
3. get pid that you want for example 15544 
5. enter win
6. type power shell
7. **get how long a process runs type below**
```shell
New-TimeSpan(Get-Process -Id 15544).StartTime
```
8. get information
```shell
Days              : 0
Hours             : 1
Minutes           : 28
Seconds           : 38
Milliseconds      : 505
Ticks             : 53185054760
TotalDays         : 0.0615567763425926
TotalHours        : 1.47736263222222
TotalMinutes      : 88.6417579333333
TotalSeconds      : 5318.505476
TotalMilliseconds : 5318505.476
```
9. **get process start time**
```shell
Get-Process -Id 15544 | select StartTime
```
10. get info
```shell
StartTime
---------
2022/3/1 上午 08:29:39
```




## reference
* [Use PowerShell to Easily Find How Long a Process Runs - **Microsoft**](https://webcache.googleusercontent.com/search?q=cache:ufcr0d_MvNQJ:https://devblogs.microsoft.com/scripting/powertip-use-powershell-to-easily-find-how-long-a-process-runs/+&cd=14&hl=zh-TW&ct=clnk&gl=tw)
* [Get-Process - **Microsoft doc**](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-process?view=powershell-7.2) 
* [How to get the process start time in PowerShell - **Stack overflow (gwtharg)**](https://stackoverflow.com/questions/34142041/how-to-get-the-process-start-time-in-powershell)
