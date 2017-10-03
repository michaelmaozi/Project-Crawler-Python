# Project-WebCrawler-Python
## 爬虫架构主体
1. 爬虫调度端 
2. URL 管理器
    - 防止重复抓取，循环抓取
    - 实现方式: 
        1.python 内存 set() - python 的set 是没有重复element的.
        2.DB(sql / nosql)
        3.缓存数据库 redis，set
3. 网页下载器
    - 把网页下载到本地，html格式或者是内存字符串
    - urllib2（python 官方的）
    - requests （python 第三方的库，更为强大）
4. 网页解析器 -> (解析出来有用的URL,可以补充到 URL管理器进行下一次的爬取)
5. 价值数据 