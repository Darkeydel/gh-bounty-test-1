# g5 camo / image-proxy probe (own content, authorized)

## c1 raw.githubusercontent svg
![rawsvg](https://raw.githubusercontent.com/Darkeydel/gh-bounty-test-1/main/x.svg)

## c2 external https png
![ext](https://example.com/x.png)

## c3 external http png
![ext-http](http://example.com/x.png)

## c4 external https svg
![ext-svg](https://example.com/x.svg)

## c5 data uri
![data](data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg"/><script>alert(1)</script>)

## c6 markdown img tag external
<img src="https://example.com/x.png">

## c7 camo direct probe target
![camo-target](https://camo.githubusercontent.com/test)

## c8 my pages svg through camo
![pages-svg](https://darkeydel.github.io/x.svg)

## c9 my pages html through camo
![pages-html](https://darkeydel.github.io/camo-target.html)

## c10 html content-type upstream through camo
![html-upstream](https://example.com/)
