# nmap 

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:31 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp80/tcp_80_http_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp80/xml/tcp_80_http_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.0031s latency).
Scanned at 2025-02-08 02:17:32 EST for 180s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 64 Apache httpd 2.2.8 ((Ubuntu) DAV/2)
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=192.168.190.129
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 32
|     Comment: 
|         
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 571
|     Comment: 
|         /* default tab styles */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 367
|     Comment: 
|         /* message boxes: warning, error, confirmation */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 642
|     Comment: 
|         /* end topmenu */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 194
|     Comment: 
|         /* even items 2,4,6,8,... */
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 23
|     Comment: 
|         
|         
|         
|         
|         		***********************************************/
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 677
|     Comment: 
|         /* table stats */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 854
|     Comment: 
|         /* end serverstatus */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 589
|     Comment: 
|         /* enabled drop/empty tabs */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 4
|     Comment: 
|         /* Main Menu Item widths */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 231
|     Comment: 
|         /**
|          * marks table rows/cells if the db field is in a where condition
|          */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 200
|     Comment: 
|         /* odd table rows 1,3,5,7,... */
|     
|     Path: http://192.168.190.129:80/mutillidae/javascript/ddsmoothmenu/jquery.min.js
|     Line number: 19
|     Comment: 
|         /*"}},lastModified:{},ajax:function(M){M=o.extend(true,M,o.extend(true,{},o.ajaxSettings,M));var W,F=/=\?(&|$)/g,R,V,G=M.type.toUpperCase();if(M.data&&M.processData&&typeof M.data!=="string"){M.data=o.param(M.data)}if(M.dataType=="jsonp"){if(G=="GET"){if(!M.url.match(F)){M.url+=(M.url.match(/\?/)?"&":"?")+(M.jsonp||"callback")+"=?"}}else{if(!M.data||!M.data.match(F)){M.data=(M.data?M.data+"&":"")+(M.jsonp||"callback")+"=?"}}M.dataType="json"}if(M.dataType=="json"&&(M.data&&M.data.match(F)||M.url.match(F))){W="jsonp"+r++;if(M.data){M.data=(M.data+"").replace(F,"="+W+"$1")}M.url=M.url.replace(F,"="+W+"$1");M.dataType="script";l[W]=function(X){V=X;I();L();l[W]=g;try{delete l[W]}catch(Y){}if(H){H.removeChild(T)}}}if(M.dataType=="script"&&M.cache==null){M.cache=false}if(M.cache===false&&G=="GET"){var E=e();var U=M.url.replace(/(\?|&)_=.*?(&|$)/,"$1_="+E+"$2");M.url=U+((U==M.url)?(M.url.match(/\?/)?"&":"?")+"_="+E:"")}if(M.data&&G=="GET"){M.url+=(M.url.match(/\?/)?"&":"?")+M.data;M.data=null}if(M.global&&!o.active++){o.event.trigger("ajaxStart")}var Q=/^(\w+:)?\/\/([^\/?#]+)/.exec(M.url);if(M.dataType=="script"&&G=="GET"&&Q&&(Q[1]&&Q[1]!=location.protocol||Q[2]!=location.host)){var H=document.getElementsByTagName("head")[0];var T=document.createElement("script");T.src=M.url;if(M.scriptCharset){T.charset=M.scriptCharset}if(!W){var O=false;T.onload=T.onreadystatechange=function(){if(!O&&(!this.readyState||this.readyState=="loaded"||this.readyState=="complete")){O=true;I();L();T.onload=T.onreadystatechange=null;H.removeChild(T)}}}H.appendChild(T);return g}var K=false;var J=M.xhr();if(M.username){J.open(G,M.url,M.async,M.username,M.password)}else{J.open(G,M.url,M.async)}try{if(M.data){J.setRequestHeader("Content-Type",M.contentType)}if(M.ifModified){J.setRequestHeader("If-Modified-Since",o.lastModified[M.url]||"Thu, 01 Jan 1970 00:00:00 GMT")}J.setRequestHeader("X-Requested-With","XMLHttpRequest");J.setRequestHeader("Accept",M.dataType&&M.accepts[M.dataType]?M.accepts[M.dataType]+", */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 215
|     Comment: 
|         /* hovered items */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 674
|     Comment: 
|         /* end Calendar */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 290
|     Comment: 
|         /* MySQL Parser */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 131
|     Comment: 
|         /* buttons in some browsers (eg. Konqueror) are block elements,
|            this breaks design */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 616
|     Comment: 
|         /* enabled hover/active tabs */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 31
|     Comment: 
|         /* general tags */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/index.php
|     Line number: 18
|     Comment: 
|         
|         //]]>
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 522
|     Comment: 
|         /**
|          * login form
|          */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 631
|     Comment: 
|         /* to be able to cancel the bottom border, use <li class="active"> */
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 33
|     Comment: 
|         
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 702
|     Comment: 
|         /* END server privileges */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 178
|     Comment: 
|         /* revert for Gecko */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 25
|     Comment: 
|         /*background of menu items (default state)*/
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 892
|     Comment: 
|         /* height: 12em; */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 549
|     Comment: 
|         /* specific elements */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 357
|     Comment: 
|         /* no extra space in table cells */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 812
|     Comment: 
|         /* serverstatus */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 53
|     Comment: 
|         /* End */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/index.php
|     Line number: 79
|     Comment: 
|         
|         // ]]>
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 696
|     Comment: 
|         /* server privileges */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 50
|     Comment: 
|         /* Holly Hack for IE \*/
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 2
|     Comment: 
|         
|         
|         
|         
|         
|         
|         
|         			security instructors are just making all this up. -->
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 929
|     Comment: 
|         /* iconic view for ul items */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 154
|     Comment: 
|         /* classes */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 30
|     Comment: 
|         /******************************************************************************/
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 876
|     Comment: 
|         /* querybox */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 645
|     Comment: 
|         /* Calendar */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 1024
|     Comment: 
|         /* END iconic view for ul items */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 36
|     Comment: 
|         /*background of menu items during onmouseover (hover state)*/
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 223
|     Comment: 
|         /* hovered table rows */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 458
|     Comment: 
|         /* end messageboxes */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 693
|     Comment: 
|         /* END table stats */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 351
|     Comment: 
|         /* leave some space between icons and text */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 16
|     Comment: 
|         /*force hasLayout in IE7 */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 809
|     Comment: 
|         /* END user privileges */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/index.php
|     Line number: 13
|     Comment: 
|         
|         //<![CDATA[
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 926
|     Comment: 
|         /* END main page */
|     
|     Path: http://192.168.190.129:80/mutillidae/javascript/ddsmoothmenu/jquery.min.js
|     Line number: 13
|     Comment: 
|         /*
|          * Sizzle CSS Selector Engine - v0.9.3
|          *  Copyright 2009, The Dojo Foundation
|          *  Released under the MIT, BSD, and GPL Licenses.
|          *  More information: http://sizzlejs.com/
|          */
|     
|     Path: http://192.168.190.129:80/mutillidae/javascript/ddsmoothmenu/jquery.min.js
|     Line number: 1
|     Comment: 
|         /*
|          * jQuery JavaScript Library v1.3.2
|          * http://jquery.com/
|          *
|          * Copyright (c) 2009 John Resig
|          * Dual licensed under the MIT and GPL licenses.
|          * http://docs.jquery.com/License
|          *
|          * Date: 2009-02-19 17:34:21 -0500 (Thu, 19 Feb 2009)
|          * Revision: 6246
|          */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 584
|     Comment: 
|         /* disabled drop/empty tabs */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 188
|     Comment: 
|         /* odd items 1,3,5,7,... */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/index.php
|     Line number: 44
|     Comment: 
|         <!-- Login form -->
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php&username=anonymous
|     Line number: 491
|     Comment: 
|         /*HTMLFormElement*/
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 856
|     Comment: 
|         /* querywindow */
|     
|     Path: http://192.168.190.129:80/mutillidae/javascript/bookmark-site.js
|     Line number: 8
|     Comment: 
|         /* Modified heavily by Jeremy Druin */
|     
|     Path: http://192.168.190.129:80/mutillidae/javascript/bookmark-site.js
|     Line number: 2
|     Comment: 
|         
|         
|         
|         
|         	***********************************************/
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 43
|     Comment: 
|         /*Sub Menu Items width */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 40
|     Comment: 
|         /*Sub level menu items */
|     
|     Path: http://192.168.190.129:80/dvwa/
|     Line number: 61
|     Comment: 
|         <!-- end align div -->
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 897
|     Comment: 
|         /* height: 100%; */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 881
|     Comment: 
|         /* height: 15em; */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 498
|     Comment: 
|         /* forbidden, no privilegs */
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 13
|     Comment: 
|         /* Top level menu links style */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 245
|     Comment: 
|         /* IE doesnt handles 'pre' right */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 747
|     Comment: 
|         /* user privileges */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 953
|     Comment: 
|         /* list-style-image: url(./themes/original/img/s_rights.png); */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 905
|     Comment: 
|         /* main page */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 873
|     Comment: 
|         /* END querywindow */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 903
|     Comment: 
|         /* end querybox */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 208
|     Comment: 
|         /* marked table rows */
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 488
|     Comment: 
|         <!-- Begin Content -->
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 579
|     Comment: 
|         /* disabled tabs */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 164
|     Comment: 
|         /* avoid a thick line since this should be used under another fieldset */
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 31
|     Comment: 
|         
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 35
|     Comment: 
|         
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/index.php
|     Line number: 66
|     Comment: 
|         
|         // <![CDATA[
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|     Line number: 526
|     Comment: 
|         <!-- End Content -->
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 174
|     Comment: 
|         /* IE */
|     
|     Path: http://192.168.190.129:80/dvwa/
|     Line number: 57
|     Comment: 
|         <!-- <img src="dvwa/images/RandomStorm.png" /> -->
|     
|     Path: http://192.168.190.129:80/mutillidae/styles/ddsmoothmenu/ddsmoothmenu-v.css
|     Line number: 30
|     Comment: 
|         /*CSS class that's dynamically added to the currently active menu items' LI A element*/
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 551
|     Comment: 
|         /* topmenu */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 706
|     Comment: 
|         /* Heading */
|     
|     Path: http://192.168.190.129:80/phpMyAdmin/phpmyadmin.css.php?lang=en-utf-8&amp;convcharset=utf-8&amp;token=1c2a8c9dd41f8b5b34a5315bfdcd126e&amp;js_frame=right&amp;nocache=2457687151
|     Line number: 504
|     Comment: 
|_        /* disabled text */
|_http-vuln-cve2017-1001000: ERROR: Script execution failed (use -d to debug)
| http-trace: TRACE is enabled
| Headers:
| Date: Sat, 08 Feb 2025 07:17:44 GMT
| Server: Apache/2.2.8 (Ubuntu) DAV/2
| Connection: close
| Transfer-Encoding: chunked
|_Content-Type: message/http
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-php-version: Versions from logo query (less accurate): 5.1.3 - 5.1.6, 5.2.0 - 5.2.17
| Versions from credits query (more accurate): 5.2.3 - 5.2.5, 5.2.6RC3
|_Version from header x-powered-by: PHP/5.2.4-2ubuntu5.10
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Allowed User Agents: 
|     Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)
|     libwww
|     lwp-trivial
|     libcurl-agent/1.0
|     PHP/
|     Python-urllib/2.5
|     GT::WWW
|     Snoopy
|     MFC_Tear_Sample
|     HTTP::Lite
|     PHPCrawl
|     URI::Fetch
|     Zend_Http_Client
|     http client
|     PECL::HTTP
|     Wget/1.13.4 (linux-gnu)
|_    WWW-Mechanize/1.34
|_http-title: Metasploitable2 - Linux
|_http-feed: Couldn't find any feeds.
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-vhosts: 
|_128 names had status 200
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=192.168.190.129
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://192.168.190.129:80/dvwa/
|     Form id: 
|     Form action: login.php
|     
|     Path: http://192.168.190.129:80/mutillidae/index.php?page=user-info.php
|     Form id: id-bad-cred-tr
|_    Form action: ./index.php?page=user-info.php
| http-fileupload-exploiter: 
|   
|_    Couldn't find a file-type field.
| http-headers: 
|   Date: Sat, 08 Feb 2025 07:17:43 GMT
|   Server: Apache/2.2.8 (Ubuntu) DAV/2
|   X-Powered-By: PHP/5.2.4-2ubuntu5.10
|   Connection: close
|   Content-Type: text/html
|   
|_  (Request type: HEAD)
| http-sql-injection: 
|   Possible sqli for queries:
|     http://192.168.190.129:80/mutillidae/index.php?do=toggle-hints%27%20OR%20sqlspider&page=home.php
|     http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php%27%20OR%20sqlspider&username=anonymous
|     http://192.168.190.129:80/mutillidae/index.php?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?do=toggle-security%27%20OR%20sqlspider&page=home.php
|     http://192.168.190.129:80/mutillidae/index.php?page=set-background-color.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=installation.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=php-errors.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fvulnerabilities.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fhow-to-access-Mutillidae-over-Virtual-Box-network.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=change-log.htm%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=capture-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=framing.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-poll.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=secret-administrative-pages.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=home.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=arbitrary-file-inclusion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=html5-storage.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=site-footer-xss-discussion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=usage-instructions.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=captured-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=notes.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=dns-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=pen-test-tool-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/dav/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://192.168.190.129:80/dav/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.190.129:80/dav/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.190.129:80/dav/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?do=toggle-hints%27%20OR%20sqlspider&page=home.php
|     http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php%27%20OR%20sqlspider&username=anonymous
|     http://192.168.190.129:80/mutillidae/index.php?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?do=toggle-security%27%20OR%20sqlspider&page=home.php
|     http://192.168.190.129:80/mutillidae/index.php?page=set-background-color.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=installation.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=php-errors.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fvulnerabilities.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fhow-to-access-Mutillidae-over-Virtual-Box-network.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=change-log.htm%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=capture-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=framing.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-poll.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=secret-administrative-pages.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=home.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=arbitrary-file-inclusion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=html5-storage.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=site-footer-xss-discussion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=usage-instructions.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=captured-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=notes.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=dns-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=pen-test-tool-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php%27%20OR%20sqlspider&username=anonymous
|     http://192.168.190.129:80/mutillidae/index.php?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=set-background-color.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=installation.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fhow-to-access-Mutillidae-over-Virtual-Box-network.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fvulnerabilities.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=capture-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=change-log.htm%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=framing.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=home.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=secret-administrative-pages.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=arbitrary-file-inclusion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-poll.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=html5-storage.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=dns-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=captured-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=site-footer-xss-discussion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=pen-test-tool-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php%27%20OR%20sqlspider&username=anonymous
|     http://192.168.190.129:80/mutillidae/index.php?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=set-background-color.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=installation.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-poll.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fvulnerabilities.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fhow-to-access-Mutillidae-over-Virtual-Box-network.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=change-log.htm%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=capture-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=framing.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=secret-administrative-pages.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=home.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=site-footer-xss-discussion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=arbitrary-file-inclusion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=html5-storage.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=dns-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=captured-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=pen-test-tool-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php%27%20OR%20sqlspider&username=anonymous
|     http://192.168.190.129:80/mutillidae/index.php?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=set-background-color.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=installation.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fvulnerabilities.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fhow-to-access-Mutillidae-over-Virtual-Box-network.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=change-log.htm%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=capture-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=framing.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-poll.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=secret-administrative-pages.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=home.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=site-footer-xss-discussion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=arbitrary-file-inclusion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=html5-storage.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=captured-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=dns-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=pen-test-tool-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=register.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.owasp.org%2Findex.php%2FLouisville
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.room362.com%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php%27%20OR%20sqlspider&username=anonymous
|     http://192.168.190.129:80/mutillidae/index.php?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.owasp.org
|     http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.php.net%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fpauldotcom.com%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.irongeek.com%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.isd-podcast.com%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=change-log.htm%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=set-background-color.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=installation.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.issa-kentuckiana.org%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=https%3A%2F%2Faddons.mozilla.org%2Fen-US%2Ffirefox%2Fcollections%2Fjdruin%2Fpr%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fvulnerabilities.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=documentation%2Fhow-to-access-Mutillidae-over-Virtual-Box-network.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=credits.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=redirectandlog.php%27%20OR%20sqlspider&forwardurl=http%3A%2F%2Fwww.pocodoy.com%2Fblog%2F
|     http://192.168.190.129:80/mutillidae/index.php?page=capture-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=framing.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=user-poll.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=secret-administrative-pages.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=home.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=arbitrary-file-inclusion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=source-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=user-info.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=html5-storage.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=add-to-your-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=site-footer-xss-discussion.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=captured-data.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=text-file-viewer.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=login.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=dns-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=view-someones-blog.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=show-log.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/index.php?page=pen-test-tool-lookup.php%27%20OR%20sqlspider
|     http://192.168.190.129:80/mutillidae/?page=login.php%27%20OR%20sqlspider
|   Possible sqli for forms:
|     Form at path: /mutillidae/index.php, form's action: ./index.php?page=user-info.php. Fields that might be vulnerable:
|_      username
| http-grep: 
|   (1) http://192.168.190.129:80/dav/: 
|     (1) ip: 
|       + 192.168.190.129
|   (3) http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php: 
|     (2) ip: 
|       + 192.168.190.128
|       + 192.168.255.255
|     (1) email: 
|       + abuse@iana.org
|   (1) http://192.168.190.129:80/mutillidae/index.php?page=credits.php: 
|     (1) email: 
|_      + mutillidae-development@gmail.com
|_http-malware-host: Host appears to be clean
|_http-server-header: Apache/2.2.8 (Ubuntu) DAV/2
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-date: Sat, 08 Feb 2025 07:17:45 GMT; +2s from local time.
|_http-apache-negotiation: mod_negotiation enabled.
|_http-chrono: Request times for /; avg: 190.57ms; min: 162.35ms; max: 230.17ms
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=192.168.190.129
|   url                                                                method
|   http://192.168.190.129:80/phpMyAdmin/                              FORM
|   http://192.168.190.129:80/dvwa/                                    FORM
|   http://192.168.190.129:80/phpMyAdmin/index.php                     FORM
|_  http://192.168.190.129:80/mutillidae/index.php?page=user-info.php  FORM
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-mobileversion-checker: No mobile version detected.
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=192.168.190.129
|   Found the following error pages: 
|   
|   Error Code: 404
|_  	http://192.168.190.129:80/phpMyAdmin/location;
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-enum: 
|   /tikiwiki/: Tikiwiki
|   /test/: Test page
|   /phpinfo.php: Possible information file
|   /phpMyAdmin/: phpMyAdmin
|   /doc/: Potentially interesting directory w/ listing on 'apache/2.2.8 (ubuntu) dav/2'
|   /icons/: Potentially interesting folder w/ directory listing
|_  /index/: Potentially interesting folder
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /dav/
|       Other: 1
|     /dvwa/
|       Other: 1
|     /mutillidae/
|       Other: 1; php: 2
|     /mutillidae/images/
|       gif: 1; jpeg: 1; jpg: 1; png: 1
|     /mutillidae/javascript/
|       js: 1
|     /mutillidae/styles/ddsmoothmenu/
|       css: 1
|     /phpMyAdmin/
|       Other: 1; css: 1; ico: 1; php: 2
|     /twiki/
|       Other: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /mutillidae/styles/ddsmoothmenu/
|   Total files found (by extension):
|_    Other: 6; css: 2; gif: 1; ico: 1; jpeg: 1; jpg: 1; js: 1; php: 4; png: 1
| http-unsafe-output-escaping: 
|   Characters [> " '] reflected in parameter page at http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php&username=anonymous
|   Characters [> " '] reflected in parameter username at http://192.168.190.129:80/mutillidae/index.php?page=password-generator.php&username=anonymous
|   Characters [> " '] reflected in parameter page at http://192.168.190.129:80/mutillidae/index.php?page=user-info.php
|   Characters [> " '] reflected in parameter page at http://192.168.190.129:80/mutillidae/index.php?page=browser-info.php
|_  Characters [> " '] reflected in parameter page at http://192.168.190.129:80/mutillidae/index.php?page=credits.php
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:20:32 2025 -- 1 IP address (1 host up) scanned in 181.17 seconds

```
# nikto 

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          192.168.190.129
+ Target Hostname:    192.168.190.129
+ Target Port:        80
+ Start Time:         2025-02-08 02:17:32 (GMT-5)
---------------------------------------------------------------------------
+ Server: Apache/2.2.8 (Ubuntu) DAV/2
+ /: Retrieved x-powered-by header: PHP/5.2.4-2ubuntu5.10.
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ Apache/2.2.8 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ /index: Uncommon header 'tcn' found, with contents: list.
+ /index: Apache mod_negotiation is enabled with MultiViews, which allows attackers to easily brute force file names. The following alternatives for 'index' were found: index.php. See: http://www.wisec.it/sectou.php?id=4698ebdc59d15,https://exchange.xforce.ibmcloud.com/vulnerabilities/8275
+ /: Web Server returns a valid response with junk HTTP methods which may cause false positives.
+ /: HTTP TRACE method is active which suggests the host is vulnerable to XST. See: https://owasp.org/www-community/attacks/Cross_Site_Tracing
+ /doc/: Directory indexing found.
+ /doc/: The /doc/ directory is browsable. This may be /usr/doc. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-1999-0678
+ /?=PHPB8B5F2A0-3C92-11d3-A3A9-4C7B08C10000: PHP reveals potentially sensitive information via certain HTTP requests that contain specific QUERY strings. See: OSVDB-12184
+ /?=PHPE9568F36-D428-11d2-A769-00AA001ACF42: PHP reveals potentially sensitive information via certain HTTP requests that contain specific QUERY strings. See: OSVDB-12184
+ /?=PHPE9568F34-D428-11d2-A769-00AA001ACF42: PHP reveals potentially sensitive information via certain HTTP requests that contain specific QUERY strings. See: OSVDB-12184
+ /?=PHPE9568F35-D428-11d2-A769-00AA001ACF42: PHP reveals potentially sensitive information via certain HTTP requests that contain specific QUERY strings. See: OSVDB-12184
+ /phpMyAdmin/changelog.php: phpMyAdmin is for managing MySQL databases, and should be protected or limited to authorized hosts.
+ /phpMyAdmin/ChangeLog: Server may leak inodes via ETags, header found with file /phpMyAdmin/ChangeLog, inode: 92462, size: 40540, mtime: Tue Dec  9 12:24:00 2008. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2003-1418
+ /phpMyAdmin/ChangeLog: phpMyAdmin is for managing MySQL databases, and should be protected or limited to authorized hosts.
+ /test/: Directory indexing found.
+ /test/: This might be interesting.
+ /phpinfo.php: Output from the phpinfo() function was found.
+ /phpinfo.php: PHP is installed, and a test script which runs phpinfo() was found. This gives a lot of system information. See: CWE-552
+ /icons/: Directory indexing found.
+ /icons/README: Apache default file found. See: https://www.vntweb.co.uk/apache-restricting-access-to-iconsreadme/
+ /phpMyAdmin/: phpMyAdmin directory found.
+ /phpMyAdmin/Documentation.html: phpMyAdmin is for managing MySQL databases, and should be protected or limited to authorized hosts.
+ /phpMyAdmin/README: phpMyAdmin is for managing MySQL databases, and should be protected or limited to authorized hosts. See: https://typo3.org/
+ /#wp-config.php#: #wp-config.php# file found. This file contains the credentials.
+ 8478 requests: 0 error(s) and 27 item(s) reported on remote host
+ End Time:           2025-02-08 02:18:47 (GMT-5) (75 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```
# screenshot


# whatweb

```
WhatWeb report for http://192.168.190.129:80
Status    : 200 OK
Title     : Metasploitable2 - Linux
IP        : 192.168.190.129
Country   : RESERVED, ZZ

Summary   : Apache[2.2.8], HTTPServer[Ubuntu Linux][Apache/2.2.8 (Ubuntu) DAV/2], PHP[5,5.2.4-2ubuntu5.10], WebDAV[2], X-Powered-By[PHP/5.2.4-2ubuntu5.10]

Detected Plugins:
[ Apache ]
	The Apache HTTP Server Project is an effort to develop and
	maintain an open-source HTTP server for modern operating
	systems including UNIX and Windows NT. The goal of this
	project is to provide a secure, efficient and extensible
	server that provides HTTP services in sync with the current
	HTTP standards.

	Version      : 2.2.8 (from HTTP Server Header)
	Google Dorks: (3)
	Website     : http://httpd.apache.org/

[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : Apache/2.2.8 (Ubuntu) DAV/2 (from server string)

[ PHP ]
	PHP is a widely-used general-purpose scripting language
	that is especially suited for Web development and can be
	embedded into HTML. This plugin identifies PHP errors,
	modules and versions and extracts the local file path and
	username if present.

	Version      : 5.2.4-2ubuntu5.10
	Version      : 5
	Google Dorks: (2)
	Website     : http://www.php.net/

[ WebDAV ]
	Web-based Distributed Authoring and Versioning (WebDAV) is
	a set of methods based on the Hypertext Transfer Protocol
	(HTTP) that facilitates collaboration between users in
	editing and managing documents and files stored on World
	Wide Web servers. - More Info:
	http://en.wikipedia.org/wiki/WebDAV

	Version      : 2

[ X-Powered-By ]
	X-Powered-By HTTP header

	String       : PHP/5.2.4-2ubuntu5.10 (from x-powered-by string)

HTTP Headers:
	HTTP/1.1 200 OK
	Date: Sat, 08 Feb 2025 07:17:37 GMT
	Server: Apache/2.2.8 (Ubuntu) DAV/2
	X-Powered-By: PHP/5.2.4-2ubuntu5.10
	Content-Length: 891
	Connection: close
	Content-Type: text/html



```
# scrapy

```

```
# dirbuster
## dirsearch

### directory 

```
http://192.168.190.129:80/.hta                 (Status: 403) [Size: 292]
http://192.168.190.129:80/.hta.html            (Status: 403) [Size: 297]
http://192.168.190.129:80/.hta.txt             (Status: 403) [Size: 296]
http://192.168.190.129:80/.hta.php             (Status: 403) [Size: 296]
http://192.168.190.129:80/.hta.jsp             (Status: 403) [Size: 296]
http://192.168.190.129:80/.htaccess            (Status: 403) [Size: 297]
http://192.168.190.129:80/.hta.asp             (Status: 403) [Size: 296]
http://192.168.190.129:80/.htaccess.html       (Status: 403) [Size: 302]
http://192.168.190.129:80/.htaccess.php        (Status: 403) [Size: 301]
http://192.168.190.129:80/.hta.aspx            (Status: 403) [Size: 297]
http://192.168.190.129:80/.htaccess.jsp        (Status: 403) [Size: 301]
http://192.168.190.129:80/.htpasswd            (Status: 403) [Size: 297]
http://192.168.190.129:80/.htaccess.txt        (Status: 403) [Size: 301]
http://192.168.190.129:80/.htaccess.aspx       (Status: 403) [Size: 302]
http://192.168.190.129:80/.htaccess.asp        (Status: 403) [Size: 301]
http://192.168.190.129:80/.htpasswd.html       (Status: 403) [Size: 302]
http://192.168.190.129:80/.htpasswd.asp        (Status: 403) [Size: 301]
http://192.168.190.129:80/.htpasswd.txt        (Status: 403) [Size: 301]
http://192.168.190.129:80/.htpasswd.aspx       (Status: 403) [Size: 302]
http://192.168.190.129:80/.htpasswd.php        (Status: 403) [Size: 301]
http://192.168.190.129:80/.htpasswd.jsp        (Status: 403) [Size: 301]
http://192.168.190.129:80/cgi-bin/             (Status: 403) [Size: 296]
http://192.168.190.129:80/cgi-bin/.html        (Status: 403) [Size: 301]
http://192.168.190.129:80/dav                  (Status: 200) [Size: 696]
http://192.168.190.129:80/index                (Status: 200) [Size: 891]
http://192.168.190.129:80/index.php            (Status: 200) [Size: 891]
http://192.168.190.129:80/phpinfo              (Status: 200) [Size: 48032]
http://192.168.190.129:80/phpinfo.php          (Status: 200) [Size: 48044]
http://192.168.190.129:80/phpMyAdmin           (Status: 200) [Size: 4145]
http://192.168.190.129:80/server-status        (Status: 403) [Size: 301]
http://192.168.190.129:80/test                 (Status: 200) [Size: 886]
http://192.168.190.129:80/twiki                (Status: 200) [Size: 782]
http://192.168.190.129:80/tikiwiki             (Status: 200) [Size: 316]

```
### files

```

```
# curl 

```
HTTP/1.1 200 OK
Date: Sat, 08 Feb 2025 07:17:33 GMT
Server: Apache/2.2.8 (Ubuntu) DAV/2
X-Powered-By: PHP/5.2.4-2ubuntu5.10
Content-Length: 891
Content-Type: text/html

<html><head><title>Metasploitable2 - Linux</title></head><body>
<pre>

                _                  _       _ _        _     _      ____
 _ __ ___   ___| |_ __ _ ___ _ __ | | ___ (_) |_ __ _| |__ | | ___|___ \
| '_ ` _ \ / _ \ __/ _` / __| '_ \| |/ _ \| | __/ _` | '_ \| |/ _ \ __) |
| | | | | |  __/ || (_| \__ \ |_) | | (_) | | || (_| | |_) | |  __// __/
|_| |_| |_|\___|\__\__,_|___/ .__/|_|\___/|_|\__\__,_|_.__/|_|\___|_____|
                            |_|


Warning: Never expose this VM to an untrusted network!

Contact: msfdev[at]metasploit.com

Login with msfadmin/msfadmin to get started


</pre>
<ul>
<li><a href="/twiki/">TWiki</a></li>
<li><a href="/phpMyAdmin/">phpMyAdmin</a></li>
<li><a href="/mutillidae/">Mutillidae</a></li>
<li><a href="/dvwa/">DVWA</a></li>
<li><a href="/dav/">WebDAV</a></li>
</ul>
</body>
</html>



```
# curl - robots

```

```
# enumeration
