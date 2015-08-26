---
title: Export Excutable Jar / Runnable Jar
author: Hans
layout: post
permalink: /2483/export-excutable-jar-runnable-jar
ect-template-is-public:
  - 
better-related-:
  - 'a:6:{s:6:"offset";s:1:"0";s:5:"stime";s:15:"1363916130.5646";s:7:"queries";s:2:"10";i:2483;a:97:{i:2790;s:15:"2.2382683753967";i:2737;s:15:"0.3327853679657";i:2734;s:16:"0.33025097846985";i:2569;s:16:"0.33240181207657";i:2563;s:16:"0.34651938080788";i:2711;s:16:"0.39643213152885";i:2714;s:15:"1.9817165136337";i:2650;s:1:"0";i:2626;s:1:"0";i:2615;s:15:"20.789144609458";i:2576;s:16:"0.37987226247787";i:2585;s:16:"0.45810860395432";i:2602;s:16:"0.45418354868889";i:2583;s:16:"0.41997930407524";i:2539;s:15:"23.109224412924";i:2418;s:15:"15.024077508933";i:2511;s:15:"12.700333688742";i:2371;s:16:"0.18018466234207";i:2346;s:15:"13.975442979819";i:2306;s:16:"0.11578692495823";i:2301;s:16:"0.35320463776588";i:2297;s:1:"0";i:2283;s:15:"38.245990940107";i:2266;s:16:"0.25956791639328";i:2260;s:16:"0.14244590699673";i:2256;s:16:"0.11790030449629";i:2245;s:1:"0";i:2232;s:1:"0";i:2223;s:15:"1.9478912353516";i:2217;s:1:"0";i:2199;s:1:"0";i:2191;s:1:"0";i:2174;s:1:"0";i:2166;s:16:"0.32935866713524";i:2134;s:1:"0";i:2125;s:15:"3.8441429138184";i:2120;s:15:"1.5593241453171";i:2114;s:14:"1.878125667572";i:2109;s:15:"3.3586752414703";i:2099;s:16:"0.17267563939094";i:2017;s:16:"0.09943849593401";i:2008;s:1:"0";i:2000;s:16:"0.27808192372322";i:1996;s:16:"0.37439414858818";i:1988;s:15:"12.175501201636";i:1947;s:1:"0";i:1926;s:1:"0";i:1921;s:16:"0.19046077132225";i:1916;s:15:"11.571122739798";i:1911;s:15:"2.5783605575562";i:1892;s:1:"0";i:1881;s:15:"1.8356541395187";i:1876;s:16:"0.36690086126327";i:1864;s:15:"2.4225475788116";i:1847;s:1:"0";i:1832;s:15:"2.7396333217621";i:1823;s:15:"18.574686620719";i:1810;s:1:"0";i:1793;s:14:"1.352814912796";i:1767;s:16:"0.32745912671089";i:1758;s:15:"2.6589047908783";i:1755;s:1:"0";i:1748;s:1:"0";i:1732;s:15:"12.553629014975";i:1704;s:15:"1.4812294244766";i:1711;s:16:"0.39216655492783";i:1706;s:1:"0";i:1697;s:15:"2.4994130134583";i:1693;s:16:"0.19335107505321";i:1680;s:16:"0.42708599567413";i:1612;s:16:"0.14963756501675";i:1558;s:16:"0.36468890309334";i:1569;s:15:"29.136485048307";i:1554;s:1:"0";i:1529;s:1:"0";i:1511;s:1:"0";i:1469;s:16:"0.42339527606964";i:1431;s:15:"0.1819434762001";i:1433;s:16:"0.19339625537395";i:1409;s:16:"0.34271124005318";i:1359;s:16:"0.27018228173256";i:2395;s:16:"0.16017508506775";i:1355;s:1:"0";i:1328;s:1:"0";i:1255;s:14:"21.13456544686";i:1257;s:15:"33.896701046003";i:1197;s:16:"0.33856430649757";i:1115;s:1:"0";i:1099;s:16:"0.28941136598587";i:1096;s:15:"1.4063634872436";i:1091;s:1:"0";i:2475;s:15:"2.7378046512604";i:2479;s:15:"5.1443195343018";i:2491;s:15:"16.703443620688";i:2485;s:15:"52.477435869236";i:2496;s:15:"17.312231157309";i:2501;s:15:"10.057413611895";}s:5:"etime";s:15:"1363916130.6166";s:5:"ctime";s:10:"1363916130";}'
views:
  - 905
bot_views:
  - 46
categories:
  - Eclipse
  - Java
tags:
  - Eclipse
  - excutable jar
  - 'JAR: Could not find the main class.'
  - Java
  - runnable jar
---
用比較舊版本的 Eclipse 匯出 JAR 的時候會出現 <span style="color: #ff0000;"><strong>JAR: Could not find the main class.</strong></span> 今天把做好的 swing 專案匯出成 JAR，在桌面點兩下什麼事情都沒發生 &#8230; 遇到問題最害怕的是什麼錯誤訊息都沒有，該從何查起 &#8230;

<!--more-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

在 **<a href="http://wazai.net/2485/jar-could-not-find-the-main-class" target="_blank">JAR: Could not find the main class.</a>** 中有提到，在 cmd 下輸入 java -jar xxxx.jar 就可以顯示錯誤訊息

<pre class="brush: shell; gutter: true">C:\Documents and Settings\user\桌面&gt;java -jar xpath.jar Exception in thread "main" java.lang.NoClassDefFoundError: com/gargoylesoftware/htmlunit/FailingHttpStatusCodeException Caused by: java.lang.ClassNotFoundException: com.gargoylesoftware.htmlunit.FailingHttpStatusCodeException
        at java.net.URLClassLoader$1.run(Unknown Source)
        at java.security.AccessController.doPrivileged(Native Method)
        at java.net.URLClassLoader.findClass(Unknown Source)
        at java.lang.ClassLoader.loadClass(Unknown Source)
        at sun.misc.Launcher$AppClassLoader.loadClass(Unknown Source)
        at java.lang.ClassLoader.loadClass(Unknown Source)
Could not find the main class: xpath.tree.Xpath. Program will exit.</pre>

這時候想起之前是用 **<a href="http://fjep.sourceforge.net/" target="_blank">Fat Jar</a>**  搞定的，去下載了 fat jar 的 lib 之後，放入 eclipse plugin 內，成功的匯出了一個 fatjar.jar，點兩下，確定可以執行 ~ 過不久即發現 &#8230; <span style="color: #000000;">原來 <strong>Eclipse 3.4</strong> 以上就已經有包含 fat jar 了，</span>  
在要匯出的專案上按<span style="color: #ff0000;"><strong>右鍵</strong> -> <strong>Export </strong>-> <strong>Runnable JAR file</strong></span>

在 library handling 的部分，可以挑選自己想要的方式

  1. <span style="color: #ff00ff;"><strong>Extract required libraries into generated JAR</strong></span>  
    把所有的 import JAR 都拆開來，包含在 JAR 的各個目錄中，ex. net/org/xxx.class
  2. <span style="color: #ff00ff;"><strong></strong><strong>Package required libraries into generated JAR</strong></span>  
    把所有的 import JAR 都包在 JAR 的根目錄下
  3. <span style="color: #ff00ff;"><strong></strong><strong></strong><strong>Copy required libraries into a sub-folder next to the generated JAR</strong></span>  
    把所有 import JAR 放在 JAR 外面獨立一個資料夾

好物一枚!!! ^__^

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
      JAR: Could not find the main class. @ 蛙齋
    </address>
    
    <address>
      <a href="http://wazai.net/2485/jar-could-not-find-the-main-class" target="_blank">http://wazai.net/2485/jar-could-not-find-the-main-class</a>
    </address>