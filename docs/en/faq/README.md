# FAQ

### What is Crawlab?

Crawlab is an open-source web crawler management platform. Its design goal is to help users easily create, manage, and
monitor web crawler tasks. Crawlab provides a user-friendly graphical interface that allows users to configure crawler
tasks, set crawling rules, monitor the crawling status, and view the crawling results.

You can check the [Introduction section](../guide) for more information.

### Why can Crawlab execute crawlers written in different programming languages and frameworks?

Crawlab executes crawler tasks based on Shell commands. Therefore, theoretically, any crawler that can be run using
Shell commands can be executed in Crawlab if the environment allows.

The `Execution Command` and `Parameters` in the crawler are concatenated to form the actual Shell command for the
crawler task. For example, if the `Execute Command` of a certain crawler is `python main.py` and the parameter
is `spider1`, then the Shell command for the crawler task will be `python main.py spider1`.

### Why does Crawlab always pull version v0.6.0 instead of the latest version?

For users in China, it is highly possible that you have configured the Aliyun mirror proxy. Please use other mirror
proxies, such as [Tencent Cloud mirror proxy](https://mirror.ccs.tencentyun.com).

### Does Crawlab support Scrapy?

Yes, Crawlab supports Scrapy, and it has a built-in pipeline that can be used. You just need to
add `crawlab.CrawlabPipeline` to the `ITEM_PIPELINS` in the `settings.py` file to integrate it.

For more details, please refer to [Spider Integration](../guide/spider/integration.md).

### Does Crawlab support Selenium?

Yes, Crawlab supports Selenium for web scraping. For more details, please refer
to [Selenium Spider Integration](../guide/spider/selenium.md).