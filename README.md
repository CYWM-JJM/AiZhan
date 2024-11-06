# AiZhan

## 说明

爱站（Aizhan）是一个中国知名的网站工具平台，以下是对其的详细介绍：

- **网站SEO数据查询**：允许用户查询任何网站的搜索引擎优化（SEO）相关数据，如百度权重、谷歌PR值（虽然谷歌PR值已停止更新，但爱站可能提供基于历史数据的分析或替代指标）、反向链接数量等。
- **Whois信息查询**：提供域名的注册信息查询服务，帮助用户了解特定网站的域名注册详情。
- **网站速度测试**：测试网站页面加载速度，分析可能影响速度的因素，帮助用户优化网站性能。
- **友链检测**：检查网站之间的友情链接质量，确保链接伙伴的网站没有负面影响，有助于维护网站的SEO健康。
- **关键词推荐与挖掘**：根据用户输入的关键词，推荐相关的热门搜索词和长尾关键词，帮助用户优化网站内容，提高搜索引擎排名。

**作为白帽，此工具主要帮助大家批量查询域名的权重，补天漏洞平台的权重信息重要以爱站为主，在漏洞挖掘过程中方便查询域名信息，维护网络空间安全。**

## 使用

工具内部已经帮大家做域名处理了，主要是去除协议头部以及端口，转换大致如下：

**注：**使用过程中如果出现问题请检查是否能够访问网站：`https://www.aizhan.com`

```
http://www.baidu.com       ->   www.baidu.com
https://www.baidu.com      ->   www.baidu.com
http://www.baidu.com:80    ->   www.baidu.com
www.baidu.com:80           ->   www.baidu.com
www.baidu.com:443          ->   www.baidu.com
```

#### 帮助

查询完成后会在当前目录下生成一个当前时间命名的`.csv`文件保存执行结果。

```
E:\self_tools\AiZhan>AiZhan.exe --help
usage: AiZhan.exe [-h] [-u URL] [-f FILE]

网站权重查询

options:
  -h, --help            show this help message and exit
  -u URL, --url URL     查询单个域名权重！
  -f FILE, --file FILE  批量查询域名权重！
```

#### 单域名查询

```
E:\self_tools\AiZhan>AiZhan.exe -u baidu.com
[2024-11-01 18:27:56] [Info] > 域名: baidu.com 查询完成(20241101182756.csv)
```

![image-20241101183626260](https://github.com/CYWM-JJM/AiZhan/blob/master/image/image-20241101183626260.png)

#### 批量域名查询

创建一个文件存放域名。

![image-20241101183943123](https://github.com/CYWM-JJM/AiZhan/blob/master/image/image-20241101183943123.png)

```
E:\self_tools\AiZhan>AiZhan.exe -f ./domains.txt
[2024-11-01 18:40:24] [Info] > 创建文件并进行初始化完成: 20241101184024.csv
Processing items: 100%|███████████████████████████| 2/2 [00:02<00:00,  1.34s/it]
[2024-11-01 18:40:27] [Info] > 终于查完了！！
```

![image-20241101184140275](https://github.com/CYWM-JJM/AiZhan/blob/master/image/image-20241101184140275.png)

#### 执行结果

![image-20241101184251560](https://github.com/CYWM-JJM/AiZhan/blob/master/image/image-20241101184251560.png)
