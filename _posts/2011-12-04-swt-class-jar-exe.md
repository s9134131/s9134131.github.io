---
title: 'SWT Class -> JAR -> EXE'
author: Hans
layout: post
permalink: /1255/swt-class-jar-exe
views:
  - 309
better-related-:
  - 'a:6:{s:6:"offset";s:1:"0";s:5:"stime";s:15:"1363862563.2872";s:7:"queries";s:1:"9";i:1255;a:97:{i:2790;s:15:"1.8953315019607";i:2737;s:1:"0";i:2734;s:1:"0";i:2569;s:1:"0";i:2563;s:1:"0";i:2711;s:1:"0";i:2714;s:14:"1.601830124855";i:2650;s:1:"0";i:2626;s:1:"0";i:2615;s:1:"0";i:2576;s:1:"0";i:2585;s:1:"0";i:2602;s:1:"0";i:2583;s:1:"0";i:2539;s:15:"1.7146654129028";i:2418;s:15:"7.3506695966784";i:2511;s:15:"7.0837585668627";i:2371;s:1:"0";i:2346;s:13:"9.63225660134";i:2306;s:1:"0";i:2301;s:1:"0";i:2297;s:1:"0";i:2283;s:15:"17.535791252143";i:2266;s:1:"0";i:2260;s:1:"0";i:2256;s:1:"0";i:2245;s:1:"0";i:2232;s:1:"0";i:2223;s:15:"1.3554869890213";i:2217;s:1:"0";i:2199;s:1:"0";i:2191;s:1:"0";i:2174;s:1:"0";i:2166;s:1:"0";i:2134;s:1:"0";i:2125;s:15:"2.2226555347443";i:2120;s:15:"1.2721474170685";i:2114;s:15:"1.5458700656891";i:2109;s:15:"2.8732488155365";i:2099;s:1:"0";i:2017;s:1:"0";i:2008;s:1:"0";i:2000;s:1:"0";i:1996;s:1:"0";i:1988;s:15:"8.0114587287966";i:1947;s:1:"0";i:1926;s:1:"0";i:1921;s:1:"0";i:1916;s:15:"7.1995678882662";i:1911;s:15:"1.4588079452515";i:1892;s:1:"0";i:1881;s:15:"1.6011307239532";i:1876;s:1:"0";i:1864;s:16:"0.85206311941147";i:1847;s:1:"0";i:1832;s:16:"0.96812999248505";i:1823;s:1:"0";i:1810;s:1:"0";i:1793;s:1:"0";i:1767;s:1:"0";i:1758;s:15:"1.4550148248673";i:1755;s:1:"0";i:1748;s:1:"0";i:1732;s:15:"8.5536290149752";i:1704;s:15:"1.4812294244766";i:1711;s:1:"0";i:1706;s:1:"0";i:1697;s:1:"0";i:1693;s:1:"0";i:1680;s:1:"0";i:1612;s:1:"0";i:1558;s:1:"0";i:1569;s:15:"15.016088936812";i:1554;s:1:"0";i:1529;s:1:"0";i:1511;s:1:"0";i:1469;s:1:"0";i:1431;s:1:"0";i:1433;s:1:"0";i:1409;s:1:"0";i:1359;s:1:"0";i:2395;s:1:"0";i:1355;s:1:"0";i:1328;s:1:"0";i:1257;s:14:"8.114799269212";i:1197;s:1:"0";i:1115;s:1:"0";i:1099;s:1:"0";i:1096;s:1:"0";i:1091;s:1:"0";i:2483;s:15:"11.220204446799";i:2475;s:15:"2.3880224227905";i:2479;s:15:"1.2790590524673";i:2491;s:15:"10.454147909171";i:2485;s:15:"11.124130912793";i:2496;s:15:"10.792707059867";i:2501;s:15:"5.6611295681063";}s:5:"etime";s:15:"1363862563.3081";s:5:"ctime";s:10:"1363862563";}'
bot_views:
  - 176
categories:
  - Java
tags:
  - fatjar
  - jar to exe
  - jar2exe
  - Java
  - SWT
---
讓 SWT Class 封裝出來的 JAR 檔可以直接滑鼠擊點兩下就執行，試了好久，終於 … 這篇文章記錄讓 SWT Class 封裝成可以直接點兩下就執行的 JAR file (eclipse fat-jar plug-in)，並且把它轉成 EXE file (JSmooth)。  
<!--more-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

###### ● 安裝 eclipse fat-jar 外掛

<p style="padding-left: 30px;">
  1. 下載 fat-jar plug-in。<a href="http://fjep.sourceforge.net/" target="_blank">下載頁面</a>。
</p>

<p style="padding-left: 30px;">
  2. 解壓縮下載回來的檔案，得到 net.sf.fjep.fatjar_0.0.31.jar，把這個檔案附置到 eclipse 安裝目錄下的 plugins 目錄裡。
</p>

<p style="padding-left: 30px;">
  3. 開啟 eclipse，在專案上按滑鼠右鍵，出現 Build Fat Jar 表示安裝完成。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar1.png" target="_blank" rel="lightbox[1255]" title="fatjar1"><img class="alignnone size-full wp-image-1309" title="fatjar1" src="http://wazai.net/wp-content/uploads/2011/12/fatjar1.png" alt="" width="330" height="682" /></a>
</p>

###### ● **用 fat-jar 產生 JAR file**

  1. 要產生可以直接執行的 JAR file，必須要一併封裝比較新版本的 swt，這邊我們使用 3.4 final release 版本，3.4 把一些必須的 dll 檔都包含在 jar file 裡面。<a href="http://www.eclipse.org/downloads/download.php?file=/eclipse/downloads/drops/R-3.4-200806172000/swt-3.4-win32-win32-x86.zip" target="_blank">下載頁面</a>。
  2. 下載完後，隨便解壓縮到一個資料夾就可以了。接著在專案上點選滑鼠右鍵，選擇新增外部保存檔。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar3.png" target="_blank" rel="lightbox[1255]" title="fatjar3"><img class="alignnone size-full wp-image-1310" title="fatjar3" src="http://wazai.net/wp-content/uploads/2011/12/fatjar3.png" alt="" width="444" height="563" /></a>
  3. 選擇剛剛解壓縮完的資料夾，裡面有個 swt.jar，按下開啟舊檔。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar4.png" target="_blank" rel="lightbox[1255]" title="fatjar4"><img class="alignnone size-full wp-image-1311" title="fatjar4" src="http://wazai.net/wp-content/uploads/2011/12/fatjar4.png" alt="" width="445" height="350" /></a>
  4. 在 eclipse 左側看到已經引入外部套件。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar5.png" target="_blank" rel="lightbox[1255]" title="fatjar5"><img class="alignnone size-full wp-image-1312" title="fatjar5" src="http://wazai.net/wp-content/uploads/2011/12/fatjar5.png" alt="" width="284" height="348" /></a>
  5. 在專案上點滑鼠右鍵，接著選擇 Build Fat Jar。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar1.png" target="_blank" rel="lightbox[1255]" title="fatjar1"><img class="alignnone size-full wp-image-1309" title="fatjar1" src="http://wazai.net/wp-content/uploads/2011/12/fatjar1.png" alt="" width="330" height="682" /></a>
  6. 更改 Jar-Name，並選擇 Main-Class，點選下一步。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar2.png" target="_blank" rel="lightbox[1255]" title="fatjar2"><img class="alignnone size-full wp-image-1313" title="fatjar2" src="http://wazai.net/wp-content/uploads/2011/12/fatjar2.png" alt="" width="446" height="452" /></a>
  7. 使用我們剛導入的 swt.jar 並且取消原本版本較舊的 swt。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar6.png" target="_blank" rel="lightbox[1255]" title="fatjar6"><img class="alignnone size-full wp-image-1314" title="fatjar6" src="http://wazai.net/wp-content/uploads/2011/12/fatjar6.png" alt="" width="446" height="452" /></a>
  8. 按下完成後，就可以在專案的資料夾裡找到剛剛建立的 test-fat.jar。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/fatjar7.png" target="_blank" rel="lightbox[1255]" title="fatjar7"><img class="alignnone size-full wp-image-1315" title="fatjar7" src="http://wazai.net/wp-content/uploads/2011/12/fatjar7.png" alt="" width="446" height="446" /></a>
  9. 滑鼠擊點兩下，可以正確執行。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/30.png" target="_blank" rel="lightbox[1255]" title="30"><img class="alignnone size-full wp-image-1316" title="30" src="http://wazai.net/wp-content/uploads/2011/12/30.png" alt="" width="300" height="200" /></a>

<span style="color: #ff0000;"> 

<div style="text-align:center; width:100%">
</div></span>

<table width="98%" border="1">
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
      <span style="color: #ff0000;"></span>
    </td>
  </tr>
</table>

<!--nextpage-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

###### ● ******將 JAR 轉成 EXE**

  1. 下載並安裝 JSmooth。<a href="http://jsmooth.sourceforge.net/download.php" target="_blank">下載頁面</a>。
  2. 執行 JSmooth，Skeleton 這裡選擇 Autodownload Wrapper，為的是讓沒有 JVM 環境的使用者，能夠自動下載 JVM。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/jsmooth1.png" target="_blank" rel="lightbox[1255]" title="jsmooth1"><img class="alignnone size-full wp-image-1317" title="jsmooth1" src="http://wazai.net/wp-content/uploads/2011/12/jsmooth1.png" alt="" width="450" height="550" /></a>
  3. Executable 選擇要輸出的 exe file 路徑跟檔名(一定要記得附檔名是 .exe)，要使用的 icon，最下面路徑的部分可以直接打勾。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/jsmooth2.png" target="_blank" rel="lightbox[1255]" title="jsmooth2"><img class="alignnone size-full wp-image-1318" title="jsmooth2" src="http://wazai.net/wp-content/uploads/2011/12/jsmooth2.png" alt="" width="444" height="542" /></a>
  4. Application 頁面，先把 Use an embedded jar 打勾，接著選擇剛剛建立的 test_fat.jar，Classpath 選擇新版的 swt.jar，最後上面的 Main class 就可以直接選擇不用自己輸入。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/jsmooth3.png" target="_blank" rel="lightbox[1255]" title="jsmooth3"><img class="alignnone size-full wp-image-1319" title="jsmooth3" src="http://wazai.net/wp-content/uploads/2011/12/jsmooth3.png" alt="" width="444" height="542" /></a>
  5. 點選工具列的齒輪圖案，會要求在 compile 之前先儲存專案，隨便輸入吧。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/jsmooth4.png" target="_blank" rel="lightbox[1255]" title="jsmooth4"><img class="alignnone size-full wp-image-1321" title="jsmooth4" src="http://wazai.net/wp-content/uploads/2011/12/jsmooth4.png" alt="" width="444" height="542" /></a>
  6. 按下儲存後，開始編譯動作。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/jsmooth5.png" target="_blank" rel="lightbox[1255]" title="jsmooth5"><img class="alignnone size-full wp-image-1322" title="jsmooth5" src="http://wazai.net/wp-content/uploads/2011/12/jsmooth5.png" alt="" width="443" height="330" /></a>
  7. 編譯完成後，可以看到剛剛輸出 exe file 的地方產生了一個 exe file。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/jsmooth6.png" target="_blank" rel="lightbox[1255]" title="jsmooth6"><img class="alignnone size-full wp-image-1323" title="jsmooth6" src="http://wazai.net/wp-content/uploads/2011/12/jsmooth6.png" alt="" width="441" height="482" /></a>
  8. 擊點兩下 exe file，成功。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/30.png" target="_blank" rel="lightbox[1255]" title="30"><img class="alignnone size-full wp-image-1316" title="30" src="http://wazai.net/wp-content/uploads/2011/12/30.png" alt="" width="300" height="200" /></a>

<span style="color: #ff0000;"> 

<div style="text-align:center; width:100%">
</div></span>

<table width="98%" border="1">
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
      <span style="color: #ff0000;"></span>
    </td>
  </tr>
</table>

<div class="page-links">
  <strong>頁面：</strong> <a href="http://wazai.net/1255/swt-class-jar-exe"><span class="page-num">1</span></a> <a href="http://wazai.net/1255/swt-class-jar-exe/2"><span class="page-num">2</span></a>
</div>