# matrix
a scrapy crawler demo, for crawl tabao item, just for fun.

从淘宝和天猫上爬取一部分测试数据，支持自动登录，自动设别天猫和淘宝模板，递归的爬取网页并将数据解析到本地日志文件。


#### 爬虫流程和需要解决的问题：

* 自动登录问题：许多社交网站（如微博），电商网站（如淘宝天猫）都需要登录，解决Cookie的自动更新；

* 递归抓取网页：URL嵌套爬取网页，需记录哪些网页已爬过，维护待爬取列表；

* 网页解析：XPath或正则表达式，对网页内容做预解析；


* 针对复杂网页，例如js生成的页面，如何解析；可以考虑模拟js解析器？


* 实现增量爬取：需记录哪些网页有更新，同步更新的网页数据；


* 预处理数据再加工，格式化为待使用数据格式；


* 避免Spider被封杀，被堵截：变换用户，变换agent，访问google cache，或者使用虚拟IP；

* 大规模爬取，如何并行，分布式部署，可能的性能瓶颈：多线程，网络io，memory？
