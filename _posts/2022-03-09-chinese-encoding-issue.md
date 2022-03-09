---
title: Chinese encoding issue
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-09 09:55:25 +0800
categories: []
tags: [encoding]     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
This article tell u how to simulate string write to db that come from some application.You will know how it works
<!--more-->

## Preliminary knowledge
* [getBytes - API](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html#getBytes-java.lang.String-)
> **Encodes** this String into a sequence of bytes using the named charset,storing the result into a new byte array. 
* [String - API](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html#String-byte:A-java.lang.String-) 
> Constructs a new String by **decoding** the specified array of bytes using the specified charset.


## Demo 
```java
try {
    // simulate a db charset UTF-8
    System.setOut(new PrintStream(new File("a.txt"), "UTF-8"));

    // your edit is UTF-8，complie using UTF-8
    String s = "測試";
    byte[] bs = s.getBytes("UTF-8"); //encoding to {e6,b8,ac,e8,a9,a6} 

    // for (int i = 0 ;i<bs.length;i++) {
    //     System.out.println(Integer.toHexString(bs[i]));
    // }

    // simulate get response parameter using big5
    String param = new String(bs, "Big5");// decoding bs array using Big5.You can use visit Query BIG-5 Code website using bs array,and will get 皜祈岫 decoding(e6 b8 ac e8 a9 a6)

    // simulate write to db
    System.out.println(param);//param be encoded using UTF-8 in the txt file and will see 皜祈岫 encoding utf8(e7 9a 9c e7 a5 88 e5 b2 ab)
} catch (Exception e) {

}
```
## encoding and decoding
![](../../assets/img/blog/20220309/encoding.jpg)

## reference 
* [Query BIG-5 Code - **ace33022**](https://ace33022.github.io/big5code/)
* [Query UTF-8 Code - **心缘地方**](http://www.mytju.com/classcode/tools/encode_utf8.asp)
* [如果在資料庫中原始資料就已經是亂碼的話 還有救嗎? - **JWorld@TW**](https://www.javaworld.com.tw/jute/post/view?bid=21&id=282136&tpg=1&ppg=1&sty=1&age=0#282136)
