# batch2 (sections 26-40)

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
