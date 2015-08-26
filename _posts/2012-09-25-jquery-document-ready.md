---
title: jQuery $(document).ready()
author: Hans
layout: post
permalink: /2301/jquery-document-ready
better-related-:
  - 'a:6:{s:6:"offset";s:1:"0";s:5:"stime";s:15:"1363888571.8124";s:7:"queries";s:1:"8";i:2301;a:97:{i:2790;s:15:"1.1470128297806";i:2737;s:1:"0";i:2734;s:1:"0";i:2569;s:1:"0";i:2563;s:1:"0";i:2711;s:1:"0";i:2714;s:1:"0";i:2650;s:1:"0";i:2626;s:1:"0";i:2615;s:1:"0";i:2576;s:1:"0";i:2585;s:1:"0";i:2602;s:1:"0";i:2583;s:1:"0";i:2539;s:16:"0.60377192497253";i:2418;s:1:"0";i:2511;s:1:"0";i:2371;s:1:"0";i:2346;s:1:"0";i:2306;s:1:"0";i:2297;s:15:"11.080135464668";i:2283;s:1:"0";i:2266;s:1:"0";i:2260;s:1:"0";i:2256;s:1:"0";i:2245;s:1:"0";i:2232;s:1:"0";i:2223;s:1:"0";i:2217;s:1:"0";i:2199;s:1:"0";i:2191;s:1:"0";i:2174;s:1:"0";i:2166;s:1:"0";i:2134;s:1:"0";i:2125;s:1:"0";i:2120;s:1:"0";i:2114;s:1:"0";i:2109;s:1:"0";i:2099;s:1:"0";i:2017;s:1:"0";i:2008;s:1:"0";i:2000;s:1:"0";i:1996;s:1:"0";i:1988;s:1:"0";i:1947;s:1:"0";i:1926;s:1:"0";i:1921;s:1:"0";i:1916;s:1:"0";i:1911;s:1:"0";i:1892;s:1:"0";i:1881;s:1:"0";i:1876;s:1:"0";i:1864;s:1:"0";i:1847;s:1:"0";i:1832;s:1:"0";i:1823;s:1:"0";i:1810;s:1:"0";i:1793;s:1:"0";i:1767;s:1:"0";i:1758;s:1:"0";i:1755;s:1:"0";i:1748;s:15:"3.9418931007385";i:1732;s:1:"0";i:1704;s:15:"6.0669333934784";i:1711;s:1:"4";i:1706;s:15:"9.9548759460449";i:1697;s:1:"0";i:1693;s:1:"0";i:1680;s:1:"0";i:1612;s:1:"0";i:1558;s:1:"0";i:1569;s:1:"0";i:1554;s:1:"0";i:1529;s:1:"0";i:1511;s:1:"0";i:1469;s:1:"0";i:1431;s:1:"0";i:1433;s:1:"0";i:1409;s:1:"0";i:1359;s:1:"0";i:2395;s:1:"0";i:1355;s:1:"0";i:1328;s:1:"0";i:1255;s:1:"0";i:1257;s:1:"0";i:1197;s:1:"0";i:1115;s:1:"0";i:1099;s:1:"0";i:1096;s:1:"0";i:1091;s:1:"0";i:2483;s:1:"0";i:2475;s:15:"13.323736647039";i:2479;s:15:"11.099203586578";i:2491;s:1:"0";i:2485;s:1:"0";i:2496;s:1:"0";i:2501;s:1:"0";}s:5:"etime";s:15:"1363888571.8383";s:5:"ctime";s:10:"1363888571";}'
views:
  - 478
bot_views:
  - 26
categories:
  - JavaScript
tags:
  - $.ready()
  - $(document).ready()
  - DOM
  - jQuery
---
前陣子跟新同事聊天的時候聊到，$(document).ready(function(){}});的問題，有同事就舉了個例子來說明，其實小蛙沒有真正去研究過為什麼要寫這個，只知道「寫了比較保險」，聽過例子之後恍然大悟，原來有這麼一層原因在。

<!--more-->

<p style="text-align: center;">
  <span style="color: #ff0000;"> 
  
  <div style="text-align:center; width:100%">
  </div></span>
</p>

<span style="color: #ff0000;"><strong>$(document).ready(function(){}});</strong></span> 用最最白話的方式來說，就是說<span style="color: #ff0000;"><strong>當整個HTML元素都被載入之後，才開始做以下動作</strong></span>。咦？還是覺得不重要？同事舉了一個簡單的例子

<pre class="brush: html; gutter: true">&lt;html&gt;
  &lt;head&gt;
    &lt;script type="text/javascript" src="jquery-1.8.2.min.js"&gt;&lt;/script&gt;
    &lt;script type="text/javascript"&gt;
      alert($(&#039;#mydiv&#039;).text());
    &lt;/script&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div id="mydiv"&gt;mydiv&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

上面的例子執行後會發現，alert出來空白的東西，並不符合我們的預期，預期應該要印出mydiv的字樣。如果把alert包在$(function(){}});裡面試試

<pre class="brush: html; gutter: true">&lt;html&gt;
  &lt;head&gt;
    &lt;script type="text/javascript" src="jquery-1.8.2.min.js"&gt;&lt;/script&gt;
    &lt;script type="text/javascript"&gt;
      $(function(){alert($(&#039;#mydiv&#039;).text());});
    &lt;/script&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div id="mydiv"&gt;mydiv&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

就如同預期的印出 mydiv 字樣了！會造成這個結果的原因是，head部分的JS程式碼在整個網頁還沒完整載入前就已經先執行，因此找不到 mydiv 這個 DOM 元素，而將alert程式碼放在 $(function(){}); 之中，等到整個網頁元素載入完成後才執行，自然就可以找到 mydiv 這個元素而印出當中的值了。其實這部分應該算是JavaScript基礎班，小蛙真是覺得不太好意思。

附帶一提，小蛙為什麼有時候忘記加$(function(){});也還是可以正常執行呢？是因為小蛙習慣把JavaScript寫在網頁的最後，如果沒有"意外"的話，會是可以正常執行的(寫$(function(){});是好習慣！記下來吧！)。例如：

<pre class="brush: html; gutter: true">&lt;html&gt;
  &lt;head&gt;
    &lt;script type="text/javascript" src="jquery-1.8.2.min.js"&gt;&lt;/script&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div id="mydiv"&gt;mydiv&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
&lt;script type="text/javascript"&gt;
  alert($(&#039;#mydiv&#039;).text());
&lt;/script&gt;</pre>

另外在**<a href="http://api.jquery.com/ready/" target="_blank">jQuery官網</a>**中提到

> All three of the following syntaxes are equivalent:
> 
>   * `$(document).ready(handler)`
>   * `$().ready(handler)` (this is not recommended)
>   * `$(handler)`

也就是說$(document).ready(function(){}); 可以縮寫成 $(function(){}});，這兩個是一樣的意思(既然一樣，為什麼不選短的來用呢 @@?)

更多內容可參考**<a href="http://api.jquery.com/ready/" target="_blank"> jQuery 官網</a>** 或 **<a href="https://groups.google.com/forum/?fromgroups=#!topic/jquery-/Ht6r9hTsCVs" target="_blank">此討論串</a>**。

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

&nbsp;