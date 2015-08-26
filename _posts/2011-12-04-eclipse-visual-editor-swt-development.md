---
title: Eclipse + Visual Editor = SWT Development
author: Hans
layout: post
permalink: /1257/eclipse-visual-editor-swt-development
views:
  - 476
better-related-:
  - 'a:6:{s:6:"offset";s:1:"0";s:5:"stime";s:15:"1363922422.5697";s:7:"queries";s:1:"8";i:1257;a:97:{i:2790;s:15:"1.8953315019607";i:2737;s:1:"0";i:2734;s:1:"0";i:2569;s:1:"0";i:2563;s:1:"0";i:2711;s:1:"0";i:2714;s:14:"1.601830124855";i:2650;s:1:"0";i:2626;s:1:"0";i:2615;s:15:"6.7401710542729";i:2576;s:1:"0";i:2585;s:1:"0";i:2602;s:1:"0";i:2583;s:1:"0";i:2539;s:15:"8.7533442768148";i:2418;s:15:"8.1455056461385";i:2511;s:15:"7.0218169483235";i:2371;s:1:"0";i:2346;s:15:"9.3000306877187";i:2306;s:1:"0";i:2301;s:1:"0";i:2297;s:1:"0";i:2283;s:15:"22.057003933726";i:2266;s:1:"0";i:2260;s:1:"0";i:2256;s:1:"0";i:2245;s:1:"0";i:2232;s:1:"0";i:2223;s:15:"1.3554869890213";i:2217;s:1:"0";i:2199;s:1:"0";i:2191;s:1:"0";i:2174;s:1:"0";i:2166;s:1:"0";i:2134;s:1:"0";i:2125;s:15:"2.2226555347443";i:2120;s:15:"1.2721474170685";i:2114;s:15:"1.5458700656891";i:2109;s:15:"2.8732488155365";i:2099;s:1:"0";i:2017;s:1:"0";i:2008;s:1:"0";i:2000;s:1:"0";i:1996;s:1:"0";i:1988;s:15:"7.6792328151754";i:1947;s:1:"0";i:1926;s:1:"0";i:1921;s:1:"0";i:1916;s:14:"6.867341974645";i:1911;s:15:"1.4588079452515";i:1892;s:1:"0";i:1881;s:15:"1.6011307239532";i:1876;s:1:"0";i:1864;s:15:"1.2979493141174";i:1847;s:1:"0";i:1832;s:15:"1.4747542142868";i:1823;s:15:"5.7856821807912";i:1810;s:1:"0";i:1793;s:1:"0";i:1767;s:1:"0";i:1758;s:15:"1.4550148248673";i:1755;s:1:"0";i:1748;s:1:"0";i:1732;s:15:"8.2214031013539";i:1704;s:15:"1.4812294244766";i:1711;s:1:"0";i:1706;s:1:"0";i:1697;s:1:"0";i:1693;s:1:"0";i:1680;s:1:"0";i:1612;s:1:"0";i:1558;s:1:"0";i:1569;s:15:"16.012766677676";i:1554;s:1:"0";i:1529;s:1:"0";i:1511;s:1:"0";i:1469;s:1:"0";i:1431;s:1:"0";i:1433;s:1:"0";i:1409;s:1:"0";i:1359;s:1:"0";i:2395;s:1:"0";i:1355;s:1:"0";i:1328;s:1:"0";i:1255;s:14:"8.777562577067";i:1197;s:1:"0";i:1115;s:1:"0";i:1099;s:1:"0";i:1096;s:16:"0.54057818651199";i:1091;s:1:"0";i:2483;s:15:"12.407421547709";i:2475;s:15:"2.3880224227905";i:2479;s:15:"1.2790590524673";i:2491;s:15:"10.121921995549";i:2485;s:15:"13.515553889481";i:2496;s:15:"10.460481146245";i:2501;s:14:"5.328903654485";}s:5:"etime";s:15:"1363922422.6133";s:5:"ctime";s:10:"1363922422";}'
bot_views:
  - 190
categories:
  - Java
tags:
  - Eclipse
  - Java
  - SWT
  - Visual Editor
---
這篇文章小蛙整理以前(2009年)的文章，主要內容是記錄怎樣使用外掛 <span style="color: #ff0000;"><strong>Visual Editor</strong></span> 讓 <span style="color: #ff0000;"><strong>Eclipse</strong></span> 可以用拖拉的方式來撰寫圖形化程式。  
<!--more-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

###### ● 安裝 Eclipse + 語言包

  1. 下載安裝 Eclipse。(**Visual Editor** final release 1.2 適用於 Eclipse 3.2 版)，所以建議使用 Eclipse 3.2。<a href="http://www.eclipse.org/downloads/" target="_blank">Eclipse 下載頁面</a>。因為小蛙本身需要做 JSP 的開發，所以直接下載 **Eclipse **+ **Lomboz** 的版本。<a href="http://lomboz.ow2.org/downloads/R-3.2.2_index.php" target="_blank">Eclipse + Lomboz 3.2.2 下載頁面</a>。
  2. 解壓縮(建議把下載回來的壓縮檔先更改名稱，有時候名稱太長在解壓縮的時候會發生錯誤)。解壓縮完後不用安裝就可以直接使用。
  3. 如果需要中文介面，可以安裝語言包。<a href="http://archive.eclipse.org/eclipse/downloads/index.php" target="_blank">中文化語言包下載頁面</a> 。最下面有個 3.2\_Language\_Packs。
  4. 解壓縮完會有 eclipse 資料夾，直接覆蓋原本解出來的 eclipse 資料夾，完成中文套件的安裝。

###### ● 安裝 Visual Editor 插件

  1. Visual Editor 可以讓 Eclipse 直接用滑鼠點選的方式，圖形化勾勒出 GUI 元件的雛形。VE 1.2 插件下載頁面。下載檔名 VE-SDK-1.2.zip 的檔案。
  2. 安裝的方法相同，解壓縮出一個 eclipse 資料夾，直接覆蓋過原本的 eclipse 資料夾即可。

###### ● 建立 SWT 類別

  1. 開啟 eclipse。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/1.png" target="_blank" rel="lightbox[1257]" title="1"><img class="alignnone size-full wp-image-1270" title="1" src="http://wazai.net/wp-content/uploads/2011/12/1.png" alt="" width="108" height="105" /></a>
  2. 歡迎畫面 (Lomboz 版本)  
    <a href="http://wazai.net/wp-content/uploads/2011/12/2.jpg" target="_blank" rel="lightbox[1257]" title="2"><img class="alignnone size-full wp-image-1272" title="2" src="http://wazai.net/wp-content/uploads/2011/12/2.jpg" alt="" width="445" height="267" /></a>
  3. 選取工作區。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/3.jpg" target="_blank" rel="lightbox[1257]" title="3"><img class="alignnone size-full wp-image-1273" title="3" src="http://wazai.net/wp-content/uploads/2011/12/3.jpg" alt="" width="445" height="254" /></a>
  4. eclipse 主畫面。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/4.jpg" target="_blank" rel="lightbox[1257]" title="4"><img class="alignnone size-full wp-image-1274" title="4" src="http://wazai.net/wp-content/uploads/2011/12/4.jpg" alt="" width="445" height="341" /></a>
  5. 新建一個 Java 專案。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/5.png" target="_blank" rel="lightbox[1257]" title="5"><img class="alignnone size-full wp-image-1275" title="5" src="http://wazai.net/wp-content/uploads/2011/12/5.png" alt="" width="310" height="442" /></a>
  6. 輸入專案名稱後按下確定。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/7.jpg" target="_blank" rel="lightbox[1257]" title="7"><img class="alignnone size-full wp-image-1276" title="7" src="http://wazai.net/wp-content/uploads/2011/12/7.jpg" alt="" width="445" height="581" /></a>
  7. 左側可以看到剛剛新增的專案以及載入的套件。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/8.jpg" target="_blank" rel="lightbox[1257]" title="8"><img class="alignnone size-full wp-image-1277" title="8" src="http://wazai.net/wp-content/uploads/2011/12/8.jpg" alt="" width="445" height="341" /></a>
  8. 我們先設定 SWT 必要的程式庫，在專案上按右鍵，點選”配置建置路徑”。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/9.jpg" target="_blank" rel="lightbox[1257]" title="9"><img class="alignnone size-full wp-image-1278" title="9" src="http://wazai.net/wp-content/uploads/2011/12/9.jpg" alt="" width="445" height="651" /></a>
  9. 選擇”新增程式庫”。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/10.jpg" target="_blank" rel="lightbox[1257]" title="10"><img class="alignnone size-full wp-image-1279" title="10" src="http://wazai.net/wp-content/uploads/2011/12/10.jpg" alt="" width="445" height="358" /></a>
 10. 選取 Standard Widget Toolkit (SWT)，下一步。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/12.jpg" target="_blank" rel="lightbox[1257]" title="12"><img class="alignnone size-full wp-image-1280" title="12" src="http://wazai.net/wp-content/uploads/2011/12/12.jpg" alt="" width="445" height="446" /></a>
 11. 點選”完成”。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/13.jpg" target="_blank" rel="lightbox[1257]" title="13"><img class="alignnone size-full wp-image-1281" title="13" src="http://wazai.net/wp-content/uploads/2011/12/13.jpg" alt="" width="445" height="445" /></a>
 12. 看到 SWT 已經增加到這個專案的程式庫裡面了。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/14.jpg" target="_blank" rel="lightbox[1257]" title="14"><img class="alignnone size-full wp-image-1282" title="14" src="http://wazai.net/wp-content/uploads/2011/12/14.jpg" alt="" width="445" height="358" /></a>
 13. 點下確定後回到主畫面，左邊多了 SWT 程式庫。  
    <a href="http://wazai.net/wp-content/uploads/2011/12/15.jpg" target="_blank" rel="lightbox[1257]" title="15"><img class="alignnone size-full wp-image-1283" title="15" src="http://wazai.net/wp-content/uploads/2011/12/15.jpg" alt="" width="445" height="341" /></a>

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

<p style="padding-left: 60px;">
  14. 接下來試試看建立 GUI 程式，在專案上點選右鍵，新建 -> Visual Class。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/16.jpg" target="_blank" rel="lightbox[1257]" title="16"><img class="alignnone size-full wp-image-1284" title="16" src="http://wazai.net/wp-content/uploads/2011/12/16.jpg" alt="" width="445" height="665" /></a>
</p>

<p style="padding-left: 60px;">
  15. 套件跟名稱隨便取，style 選取 SWT / Shell，public static void main(String[] args) 打勾後點選完成。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/17.jpg" target="_blank" rel="lightbox[1257]" title="17"><img class="alignnone size-full wp-image-1285" title="17" src="http://wazai.net/wp-content/uploads/2011/12/17.jpg" alt="" width="445" height="461" /></a>
</p>

<p style="padding-left: 60px;">
  16. 回到主畫面後可以看到剛新建立的專案，已經開啟好兩個區域，圖形化區以及程式區，將滑鼠移到右邊的 Palette 會開啟 GUI 工具。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/18.jpg" target="_blank" rel="lightbox[1257]" title="18"><img class="alignnone size-full wp-image-1286" title="18" src="http://wazai.net/wp-content/uploads/2011/12/18.jpg" alt="" width="445" height="336" /></a>
</p>

<p style="padding-left: 60px;">
  17. 我們選上面綠色箭頭旁邊的黑色小箭頭，執行為 -> SWT 應用程式。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/19.png" target="_blank" rel="lightbox[1257]" title="19"><img class="alignnone size-full wp-image-1287" title="19" src="http://wazai.net/wp-content/uploads/2011/12/19.png" alt="" width="448" height="166" /></a>
</p>

<p style="padding-left: 60px;">
  18. 出現 SWT 建立的空白視窗。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/20.png" target="_blank" rel="lightbox[1257]" title="20"><img class="alignnone size-full wp-image-1288" title="20" src="http://wazai.net/wp-content/uploads/2011/12/20.png" alt="" width="300" height="200" /></a>
</p>

<p style="padding-left: 60px;">
  19. 要新增 GUI 元件，先把 Layout 改成 null，在圖形化編輯區裡的 Shell 視窗上按右鍵，Set Layout -> 選擇 null。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/21.png" target="_blank" rel="lightbox[1257]" title="21"><img class="alignnone size-full wp-image-1289" title="21" src="http://wazai.net/wp-content/uploads/2011/12/21.png" alt="" width="477" height="514" /></a>
</p>

<p style="padding-left: 60px;">
  20. 接著到 Palette 選擇 Button。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/22.png" target="_blank" rel="lightbox[1257]" title="22"><img class="alignnone size-full wp-image-1290" title="22" src="http://wazai.net/wp-content/uploads/2011/12/22.png" alt="" width="149" height="478" /></a>
</p>

<p style="padding-left: 60px;">
  21. 輸入 Button 的名稱。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/23.jpg" target="_blank" rel="lightbox[1257]" title="23"><img class="alignnone size-full wp-image-1291" title="23" src="http://wazai.net/wp-content/uploads/2011/12/23.jpg" alt="" width="445" height="250" /></a>
</p>

<p style="padding-left: 60px;">
  22. 在 Shell 視窗中畫出一個 Button，eclipse 會自動產生相關程式碼，最下面內容的頁面也會顯示該物件的所有屬性。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/24.jpg" target="_blank" rel="lightbox[1257]" title="24"><img class="alignnone size-full wp-image-1292" title="24" src="http://wazai.net/wp-content/uploads/2011/12/24.jpg" alt="" width="445" height="463" /></a>
</p>

<p style="padding-left: 60px;">
  23. text 的地方可以設定按鈕要顯示的文字。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/25.png" target="_blank" rel="lightbox[1257]" title="25"><img class="alignnone size-full wp-image-1293" title="25" src="http://wazai.net/wp-content/uploads/2011/12/25.png" alt="" width="314" height="255" /></a>
</p>

<p style="padding-left: 60px;">
  24. 也可以直接在按鈕上面點一下滑鼠左鍵修改文字。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/26.png" target="_blank" rel="lightbox[1257]" title="26"><img class="alignnone size-full wp-image-1294" title="26" src="http://wazai.net/wp-content/uploads/2011/12/26.png" alt="" width="300" height="200" /></a>
</p>

<p style="padding-left: 60px;">
  25. 如果內容頁面沒有出現，或是需要其他頁面，可以到視窗 -> 顯示視圖中選取。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/28.png" target="_blank" rel="lightbox[1257]" title="28"><img class="alignnone size-full wp-image-1296" title="28" src="http://wazai.net/wp-content/uploads/2011/12/28.png" alt="" width="351" height="405" /></a>
</p>

<p style="padding-left: 60px;">
  26. 接著我們加入事件到這個按鈕。在按鈕上按右鍵，Events -> widgetSelected，也可以按 Add Events … 自行設定要有哪些事件。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/27.jpg" target="_blank" rel="lightbox[1257]" title="27"><img class="alignnone size-full wp-image-1295" title="27" src="http://wazai.net/wp-content/uploads/2011/12/27.jpg" alt="" width="445" height="343" /></a>
</p>

<p style="padding-left: 60px;">
  27. 執行程式，開啟主控台頁面，可以看到剛剛加入的事件。在主控台印出 widgetSelected() 的訊息。<br /> <a href="http://wazai.net/wp-content/uploads/2011/12/29.png" target="_blank" rel="lightbox[1257]" title="29"><img class="alignnone size-full wp-image-1297" title="29" src="http://wazai.net/wp-content/uploads/2011/12/29.png" alt="" width="298" height="255" /></a>
</p>

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
  <strong>頁面：</strong> <a href="http://wazai.net/1257/eclipse-visual-editor-swt-development"><span class="page-num">1</span></a> <a href="http://wazai.net/1257/eclipse-visual-editor-swt-development/2"><span class="page-num">2</span></a>
</div>