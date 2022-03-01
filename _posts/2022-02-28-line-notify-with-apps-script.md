---
title: Line notify with Apps script
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-02-28 23:11:35 +0800
categories: []
tags: [line notify,apps script]     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
This article will teach u how to crate a apps script application.
This application will send message to your line using line notify service.
<!--more-->


## lilne notify
### create line notify token
1. login in line notify
2. click right coner select box and choose person page
3. scroll down the page and publish token
4. enter your own token name
5. choose u whant group  name and click publish
6. copy token and save to other place

## apps script
### create app script application
1. login in google
2. enter https://script.google.com/home
3. click left coner plus sign to create new project
4. naming your project name
5. coding
    ```js
    function doPost(e) {
    var token = 'xxxxxxx';
    var param = e.parameter;
    var msg = param.msg;

    UrlFetchApp.fetch('https://notify-api.line.me/api/notify', {
            'headers': {
                'Authorization': 'Bearer ' + token,
            },
            'method': 'post',
            'payload': {
                'message':msg
            }
        });
    }
    ```
6. click right coner deploy icon
7. choose new deploy
8. add description...and deploy
9. Authorize...and allow
10. copy your application url

## Testing
1. open chrome console
2. load jquery
   ```js
   var jqry = document.createElement('script');
   jqry.src = "https://code.jquery.com/jquery-3.3.1.min.js";
   document.getElementsByTagName('head')[0].appendChild(jqry);
   jQuery.noConflict();
   ```
3. test code
   ```js
   $.post('your application url',
    {msg:'hello world'},
    function(e){
        console.log(e);
    });
   ```
4. get message on line app

## reference
* [Run jQuery in Chrome Console - doobom's blog](https://doobom.me/run-jquery-in-chrome-console)
* [自建 LINE Notify 訊息通知 - oxxostudio blog](https://www.oxxostudio.tw/articles/201806/line-notify.html)
* [Apps Script](https://script.google.com)