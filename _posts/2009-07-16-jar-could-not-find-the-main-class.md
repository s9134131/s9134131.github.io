---
title: 'JAR: Could not find the main class.'
author: Hans
layout: post
ect-template-is-public:
  - 
better-related-:
  - 'a:6:{s:6:"offset";s:1:"0";s:5:"stime";s:15:"1364123735.3476";s:7:"queries";s:1:"9";i:2485;a:97:{i:2790;s:15:"2.2340710163116";i:2737;s:16:"0.33092057704925";i:2734;s:16:"0.32840037345886";i:2569;s:16:"0.33053913712501";i:2563;s:16:"0.34457761049271";i:2711;s:16:"0.39421066641808";i:2714;s:15:"1.9776645898819";i:2650;s:1:"0";i:2626;s:1:"0";i:2615;s:15:"20.449127176671";i:2576;s:16:"0.37774360179901";i:2585;s:16:"0.45554155111313";i:2602;s:15:"0.4516384601593";i:2583;s:16:"0.41762590408325";i:2539;s:15:"22.766749361425";i:2418;s:15:"14.686226824193";i:2511;s:15:"12.364401081472";i:2371;s:16:"0.17917497456074";i:2346;s:15:"13.636526087194";i:2306;s:16:"0.11513810604811";i:2301;s:16:"0.35122540593147";i:2297;s:1:"0";i:2283;s:15:"37.569660145579";i:2266;s:16:"0.25811341404915";i:2260;s:16:"0.14164769649506";i:2256;s:16:"0.11723963916302";i:2245;s:1:"0";i:2232;s:1:"0";i:2223;s:15:"1.9459174871445";i:2217;s:1:"0";i:2199;s:1:"0";i:2191;s:1:"0";i:2174;s:1:"0";i:2166;s:16:"0.32751306891441";i:2134;s:1:"0";i:2125;s:15:"3.8385934829712";i:2120;s:15:"1.5561875104904";i:2114;s:15:"1.8744077682495";i:2109;s:15:"3.3525052070618";i:2099;s:16:"0.17170803248882";i:2017;s:17:"0.098881274461746";i:2008;s:1:"0";i:2000;s:16:"0.27652364969254";i:1996;s:16:"0.37229618430138";i:1988;s:15:"11.839534023671";i:1947;s:1:"0";i:1926;s:1:"0";i:1921;s:16:"0.18939350545406";i:1916;s:15:"11.234967687993";i:1911;s:15:"2.5743019580841";i:1892;s:1:"0";i:1881;s:15:"1.8324176073074";i:1876;s:16:"0.36484488844871";i:1864;s:15:"2.4194962978363";i:1847;s:1:"0";i:1832;s:15:"2.7362387180328";i:1823;s:15:"18.237046698003";i:1810;s:1:"0";i:1793;s:15:"1.3508344888687";i:1767;s:16:"0.32562416791916";i:1758;s:14:"2.654367685318";i:1755;s:1:"0";i:1748;s:1:"0";i:1732;s:15:"12.217930296331";i:1704;s:15:"1.4794509410858";i:1711;s:15:"0.3899689912796";i:1706;s:1:"0";i:1697;s:15:"2.4982826709747";i:1693;s:16:"0.19226761162281";i:1680;s:16:"0.42469277977943";i:1612;s:16:"0.14879904687405";i:1558;s:16:"0.36264532804489";i:1569;s:15:"28.463643509684";i:1554;s:1:"0";i:1529;s:1:"0";i:1511;s:1:"0";i:1469;s:16:"0.42102271318436";i:1431;s:16:"0.18092393875122";i:1433;s:16:"0.19231253862381";i:1409;s:16:"0.34079080820084";i:1359;s:16:"0.26866829395294";i:2395;s:15:"0.1592775285244";i:1355;s:1:"0";i:1328;s:1:"0";i:1255;s:15:"22.123363930522";i:1257;s:15:"34.549833235947";i:1197;s:15:"0.3366671204567";i:1115;s:1:"0";i:1099;s:15:"0.2877896130085";i:1096;s:15:"1.4038844108582";i:1091;s:1:"0";i:2483;s:15:"35.474731860367";i:2475;s:15:"2.7329773902893";i:2479;s:15:"5.1394019126892";i:2491;s:15:"16.361314752965";i:2496;s:15:"16.969735124975";i:2501;s:15:"9.7229670974305";}s:5:"etime";s:15:"1364123735.4661";s:5:"ctime";s:10:"1364123735";}'
views:
  - 272
bot_views:
  - 31
categories:
  - Eclipse
  - Java
tags:
  - Eclipse
  - 'JAR: Could not find the main class.'
  - Java
  - SWT
---
用 <span style="color: #ff0000;"><strong>Eclipse + SWT</strong></span> 開發一個英文單字練習工具，忙了半天，想說先在不同電腦中測試既有的功能，在<a href="http://wazai.net/1255/swt-class-jar-exe" target="_blank"><strong> SWT Class -> JAR -> EXE</strong></a> 文章中提到過，**怎麼讓 JAR 可以轉 EXE 並在不同電腦上執行**，結果 ~ 封裝出來的 FAT-JAR 只能在本機上執行 &#8230;

<!--more-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

把封裝好的 Jar 上傳到筆電會一直出現

<pre>Could not find the main class.</pre>

光看上面的錯誤訊息，找不到 main class?? 明明程式裡面就有 **public static void main(String[] args)**，試過各種方法，程式碼 mark 掉，再慢慢找問題，試了一個下午問題還是存在，在**<a href="http://yintel.javaeye.com/blog/374842" target="_blank"> jar文件Could not find the main class解决办法</a>** 看到一線曙光，沒想到原因竟然是程式<span style="color: #ff0000;"><strong>找不到 import 的套件</strong></span>，跟字面上理解的 main class 完全沒關係。

在 **開始 -> 執行 -> cmd** 下執行 java -jar TEST_fat.jar 後，才從錯誤訊息裡面發現，  
原來是引用 JMF 套件的時候，並沒有在 Eclipse 裡面指定外部套件，cmd 下的錯誤訊息為：

<pre class="brush: shell; gutter: true">C:\&gt;java -jar TEST_fat.jar
Exception in thread "main" java.lang.NoClassDefFoundError: javax/media/NoPlayerE
xception
Caused by: java.lang.ClassNotFoundException: javax.media.NoPlayerException
        at java.net.URLClassLoader$1.run(Unknown Source)
        at java.security.AccessController.doPrivileged(Native Method)
        at java.net.URLClassLoader.findClass(Unknown Source)
        at java.lang.ClassLoader.loadClass(Unknown Source)
        at sun.misc.Launcher$AppClassLoader.loadClass(Unknown Source)
        at java.lang.ClassLoader.loadClass(Unknown Source)
        at java.lang.ClassLoader.loadClassInternal(Unknown Source)
Could not find the main class: vocabulary.TEST. Program will exit.</pre>

這樣就比直接點兩下執行 JAR 檔出現的 &#8220;could not find the main class" 清楚多了。

<span style="color: #ff0000;"> 

<div style="text-align:center; width:100%">
</div></span>

<table width="98%" border="0">
  <tr valign="top">
    <td>
      <span style="color: #ff0000;"> <!--
<table width="98%" border="0" style="text-align:center">
  <tbody>
    <tr valign="top">
      <td>

</td>
    </tr>
  </tbody>
</table>
--></span>
    </td>
    
    <td>
    </td>
  </tr>
</table>

**參考資料：**

  1. <address>
      SWT Class -> JAR -> EXE @ 蛙齋
    </address>
    
    <address>
      <a href="http://wazai.net/1255/swt-class-jar-exe" target="_blank">http://wazai.net/1255/swt-class-jar-exe</a>
    </address>

  2. <address>
      jar文件Could not find the main class解决办法 @ 朱紫空间
    </address>
    
    <address>
      <a href="http://yintech.iteye.com/blog/374842" target="_blank">http://yintech.iteye.com/blog/374842</a>
    </address>