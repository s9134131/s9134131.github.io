---
title: Java + Excel = JXL
author: Hans
layout: post
permalink: /1569/java-excel-jxl
better-related-:
  - 'a:6:{s:6:"offset";s:1:"0";s:5:"stime";s:15:"1363866894.0016";s:7:"queries";s:1:"9";i:1569;a:97:{i:2790;s:15:"1.8953315019607";i:2737;s:1:"0";i:2734;s:1:"0";i:2569;s:1:"0";i:2563;s:1:"0";i:2711;s:15:"8.0720613937441";i:2714;s:14:"1.601830124855";i:2650;s:1:"0";i:2626;s:1:"0";i:2615;s:15:"7.0723969678942";i:2576;s:1:"0";i:2585;s:1:"0";i:2602;s:1:"0";i:2583;s:1:"0";i:2539;s:14:"9.085570190436";i:2418;s:15:"8.4777315597598";i:2511;s:15:"7.3540428619448";i:2371;s:15:"3.0009994506836";i:2346;s:13:"9.63225660134";i:2306;s:1:"0";i:2301;s:1:"0";i:2297;s:1:"0";i:2283;s:15:"22.721455760968";i:2266;s:1:"0";i:2260;s:1:"0";i:2256;s:1:"0";i:2245;s:1:"0";i:2232;s:1:"0";i:2223;s:15:"1.3554869890213";i:2217;s:1:"0";i:2199;s:1:"0";i:2191;s:1:"0";i:2174;s:1:"0";i:2166;s:1:"0";i:2134;s:1:"0";i:2125;s:15:"2.2226555347443";i:2120;s:15:"1.2721474170685";i:2114;s:15:"1.5458700656891";i:2109;s:15:"2.8732488155365";i:2099;s:1:"0";i:2017;s:1:"0";i:2008;s:1:"0";i:2000;s:1:"0";i:1996;s:1:"0";i:1988;s:15:"8.0114587287966";i:1947;s:1:"0";i:1926;s:1:"0";i:1921;s:1:"0";i:1916;s:15:"7.1995678882662";i:1911;s:15:"1.4588079452515";i:1892;s:1:"0";i:1881;s:15:"1.6011307239532";i:1876;s:1:"0";i:1864;s:15:"1.2979493141174";i:1847;s:1:"0";i:1832;s:15:"1.4747542142868";i:1823;s:15:"6.1179080944125";i:1810;s:1:"0";i:1793;s:1:"0";i:1767;s:1:"0";i:1758;s:15:"1.4550148248673";i:1755;s:1:"0";i:1748;s:1:"0";i:1732;s:15:"21.327577964808";i:1704;s:15:"1.4812294244766";i:1711;s:1:"0";i:1706;s:1:"0";i:1697;s:1:"0";i:1693;s:1:"0";i:1680;s:1:"0";i:1612;s:1:"0";i:1558;s:1:"0";i:1554;s:1:"0";i:1529;s:1:"0";i:1511;s:1:"0";i:1469;s:1:"0";i:1431;s:1:"0";i:1433;s:1:"0";i:1409;s:1:"0";i:1359;s:1:"0";i:2395;s:1:"0";i:1355;s:1:"0";i:1328;s:1:"0";i:1255;s:15:"7.7808848362032";i:1257;s:15:"14.390844055188";i:1197;s:1:"0";i:1115;s:1:"0";i:1099;s:1:"0";i:1096;s:16:"0.54057818651199";i:1091;s:1:"0";i:2483;s:15:"13.071873374952";i:2475;s:15:"2.3880224227905";i:2479;s:15:"1.2790590524673";i:2491;s:15:"10.454147909171";i:2485;s:15:"12.851102062238";i:2496;s:15:"10.792707059867";i:2501;s:15:"5.6611295681063";}s:5:"etime";s:15:"1363866894.0183";s:5:"ctime";s:10:"1363866894";}'
views:
  - 2724
bot_views:
  - 110
categories:
  - Java
tags:
  - Eclipse
  - excel
  - Java
  - JExcelApi
  - jxl
---
講到試算表，大家最熟悉的應該就是Microsoft Office Excel了吧！但其實大部分的人都只會基本的Excel操作及運算，Excel其實有很多非常強大的功能，這篇文章其實不是教大家怎麼使用Excel，小蛙也只會基本的操作，由於Excel所包含的強大功能，以致於現在有很多資料都是採用Excel儲存，像小蛙的其中一項工作就是把某些單位中的資料匯入到資料庫中，而某些單位提供給小蛙的資料就是Excel，小蛙要做的事情就是必須先從Excel中把資料截取出來，才能做後續的操作以利於塞入特定資料庫中。這篇文章要介紹怎麼使用Java讀取Excel內容。

<!--more-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

要在Java中操作Excel必須先下載<a href="http://www.andykhan.com/jexcelapi/download.html" target="_blank">Java Excel API</a>。這邊小蛙下載最新版的JExecelApi v2.6.12。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-1.png" rel="lightbox[1569]" title="jxl-1"><img class="alignnone size-full wp-image-1570" title="jxl-1" src="http://wazai.net/wp-content/uploads/2011/12/jxl-1.png" alt="" width="451" height="290" /></a>

下載到桌面後，我們只需要壓縮檔中的jxl.jar檔案，可以透過WinRAR(WinZip or 7zip &#8230;等)解壓縮軟體取得jxl.jar。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-2.png" rel="lightbox[1569]" title="jxl-2"><img class="alignnone size-full wp-image-1571" title="jxl-2" src="http://wazai.net/wp-content/uploads/2011/12/jxl-2.png" alt="" width="518" height="358" /></a>

解壓縮後可以得到jexcelapi，而我們要的jxl.jar在jexcelapi資料夾內。如果你的使用方式跟小蛙一樣，直接點兩下開啟WinRAR介面的話，就可以直接拖曳著jxl.jar到桌面，而不用解壓縮整個檔案。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-3.png" rel="lightbox[1569]" title="jxl-3"><img class="alignnone size-full wp-image-1572" title="jxl-3" src="http://wazai.net/wp-content/uploads/2011/12/jxl-3.png" alt="" width="520" height="349" /></a>

接下來要把這個jar檔放進專案中讓我們可以透過Eclipse使用，之前小蛙會將所有使用到的Library都放置在一個資料夾，讓不同專案可以去include，但後來工讀生盛哥(組內最強)建議可以每個專案中都建立一個lib資料夾，裡面專門放置這個專案會用到的函式庫，雖然可能會造成空間浪費(同一個套件複製好幾份在不同專案中)，但到時候要維護或是打包之類的會方便許多。下圖是在專案中建立一個Folder的操作，在專案上按右鍵->New->Folder。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-4.png" rel="lightbox[1569]" title="jxl-4"><img class="alignnone size-full wp-image-1573" title="jxl-4" src="http://wazai.net/wp-content/uploads/2011/12/jxl-4.png" alt="" width="519" height="325" /></a>

輸入Folder名稱。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-5.png" rel="lightbox[1569]" title="jxl-5"><img class="alignnone size-full wp-image-1574" title="jxl-5" src="http://wazai.net/wp-content/uploads/2011/12/jxl-5.png" alt="" width="525" height="578" /></a>

就會出現在Eclipse介面中的專案裡了。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-6.png" rel="lightbox[1569]" title="jxl-6"><img class="alignnone size-full wp-image-1575" title="jxl-6" src="http://wazai.net/wp-content/uploads/2011/12/jxl-6.png" alt="" width="213" height="123" /></a>

光是這樣Eclipse還沒辦法使用這個Jar的功能喔！接著我們要讓Eclipse可以"認得"這個Jar。在剛剛的jar上面點選滑鼠右鍵，選擇Build Path -> Add to Build Path。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-7.png" rel="lightbox[1569]" title="jxl-7"><img class="alignnone size-full wp-image-1576" title="jxl-7" src="http://wazai.net/wp-content/uploads/2011/12/jxl-7.png" alt="" width="541" height="433" /></a>

上圖的jxl.jar變成下圖這個樣子，並且在Referenced Libraries中出現了一個jxl.jar。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-8.png" rel="lightbox[1569]" title="jxl-8"><img class="alignnone size-full wp-image-1577" title="jxl-8" src="http://wazai.net/wp-content/uploads/2011/12/jxl-8.png" alt="" width="213" height="155" /></a>

接下來介紹JXL的使用方法。

<pre>// 要注意如果檔案路徑中有「\」必須用「\\」或「/」取代掉
// 使用JXL必須先建立一個Workbook，讀取方法如下。
// 小蛙測試的時候 xlsx 的檔案會發生錯誤
Workbook workbook = Workbook.getWorkbook(new File("E:\\鄉鎮區中英文.xls"));

// 接著建立 Sheet，Workbook可以看成是一個excel檔案，Sheet顧名思義就是一個頁籤。
// 可以直接 getSheet(0) 表示第一個頁籤(從0開始算)
// 也可以透過 getSheet("頁籤名稱") 來取得頁籤
Sheet sheet = workbook.getSheet(0);

// 讀取儲存格(Cell)的方法，getCell(Columns, Rows)，也是一樣從0開始(直,橫)
Cell c = sheet.getCell(j, i); 

// 要一列一列往下讀的方式，印出每一行的內容
for(int i = 0; i &lt; sheet.getRows(); i++){
    for(int j = 0; j &lt; sheet.getColumns(); j++){
        Cell c = sheet.getCell(j, i);
        String s = c.getContents();
        System.out.println(s);
    }
    System.out.println("-------");
}</pre>

這邊小蛙介紹一個Eclipse小技巧。把上面的程式貼在Eclipse裡面卻發現有紅色的底線，是Eclipse告訴開發者你這行程式有錯誤喔！並且提供貼心小建議，左邊有一個叉叉，點選滑鼠左鍵可以看到Eclipse給了幾個貼心的小建議，例如下圖Eclipse就告訴開發者可能是少import java.io.File; &#8230; 等等，雖然不一定每次都會正確，這個便利的設計可以讓開發者少打一些字，也可以更快找出錯誤的原因。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-9.png" rel="lightbox[1569]" title="jxl-9"><img title="jxl-9" src="http://wazai.net/wp-content/uploads/2011/12/jxl-9-580x223.png" alt="" width="580" height="223" /></a>

下圖是必須做Exception判斷。  
<a href="http://wazai.net/wp-content/uploads/2011/12/jxl-11.png" rel="lightbox[1569]" title="jxl-11"><img class="alignnone size-large wp-image-1580" title="jxl-11" src="http://wazai.net/wp-content/uploads/2011/12/jxl-11-580x250.png" alt="" width="580" height="250" /></a>

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