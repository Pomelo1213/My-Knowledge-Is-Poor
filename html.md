### 行内元素有哪些？块级元素有哪些？

行内元素：a	b	span	img	input	select 

块级元素：div	ul	ol	li	h1	h2	h3...

### html5 有哪些新特性？如何处理html5 新标签的浏览器兼容问题？

html5 新特性：

- canvas
- video 和 audio
- localStorage
- 语义化标签：article、footer、header、nav、section
- websocket

如何处理兼容：

- IE 支持通过 document.createElement方法产生的标签，通过这个特性让浏览器兼容。
- 或者使用成熟的库：html5shim。

### 简述一下你对HTML语义化的理解

- 用正确的标签做正确的事。
- 让HTML的结构更加清晰，便于搜索引擎解析，利于SEO（Search Engine Optimization）。

### 描述一下 cookies、sessionStorage 和 localStorage的区别？

- cookie 是网站为了标志用户身份而存储在用户端的数据，每一次请求都会带上cookie，cookie 在过期时间之前一直有效，即使浏览器关闭。存储大小为4K。

- sessionStorage 和 localStorage不会自动带在请求里，仅仅在本地存储。存储大小大于5M。

  sessionStorage 在浏览器关闭后自动删除，localStorage 不会自动删除，会一直存在，除非手动删除。

