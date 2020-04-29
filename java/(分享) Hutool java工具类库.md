# 简介

工欲善其事必先利其器！ 

Hutool是一个小而全的Java工具类库，通过静态方法封装，降低相关API的学习成本，提高工作效率。Hutool是项目中“util”包友好的替代，它节省了开发人员对项目中公用类和公用工具方法的封装时间，使开发专注于业务，同时可以最大限度的避免封装不完善带来的bug。

-------------------------------------------------------------------------------

# Hutool可以帮我们做什么

在我们的日常开发工作中，我们经常需要重复的去做下面的这些事情：

- 判断字符串、集合、数组是否为空

- 类型的转换

- 日期时间的处理

- IO流相关的处理，如读取配置文件

- HTTP相关，如接口的调用，JSON数据的解析与转换

- Excel读取生成

- 编码与解码

- XML数据读写

等等......

### 使用举例：

Http请求
```
//GET请求                                                                                                                   
String content = HttpUtil.get(url); 

//POST请求
HashMap<String, Object> paramMap = new HashMap<>();
paramMap.put("city", "北京");
String result1 = HttpUtil.post(url, paramMap);
```
-------------------------------------------------------------------------------

# 包含组件
一个Java基础工具类，对文件、流、加密解密、转码、正则、线程、XML等JDK方法进行封装，组成各种Util工具类，同时提供以下组件：

| 模块                |     介绍                                                                          |
| -------------------|---------------------------------------------------------------------------------- |
| hutool-aop         |     JDK动态代理封装，提供非IOC下的切面支持                                              |
| hutool-bloomFilter |     布隆过滤，提供一些Hash算法的布隆过滤                                                |
| hutool-cache       |     简单缓存实现                                                                     |
| hutool-core        |     核心，包括Bean操作、日期、各种Util等                                               |
| hutool-cron        |     定时任务模块，提供类Crontab表达式的定时任务                                          |
| hutool-crypto      |     加密解密模块，提供对称、非对称和摘要算法封装                                          |
| hutool-db          |     JDBC封装后的数据操作，基于ActiveRecord思想                                         |
| hutool-dfa         |     基于DFA模型的多关键字查找                                                         |
| hutool-extra       |     扩展模块，对第三方封装（模板引擎、邮件、Servlet、二维码、Emoji、FTP、分词等）            |
| hutool-http        |     基于HttpUrlConnection的Http客户端封装                                            |
| hutool-log         |     自动识别日志实现的日志门面                                                         |
| hutool-script      |     脚本执行封装，例如Javascript                                                     |
| hutool-setting     |     功能更强大的Setting配置文件和Properties封装                                        |
| hutool-system      |     系统参数调用封装（JVM信息等）                                                      |
| hutool-json        |     JSON实现                                                                       |
| hutool-captcha     |     图片验证码实现                                                                   |
| hutool-poi         |     针对POI中Excel和Word的封装                                                       |
| hutool-socket      |     基于Java的NIO和AIO的Socket封装                                                   |

可以根据需求对每个模块单独引入，也可以通过引入`hutool-all`方式引入所有模块。

-------------------------------------------------------------------------------

# 官方文档 

[中文文档](https://www.hutool.cn/docs/)

[参考API](https://apidoc.gitee.com/loolly/hutool/)

[视频介绍](https://www.bilibili.com/video/BV1bQ4y1M7d9?p=2)

-------------------------------------------------------------------------------

# 安装

## Maven
在项目的pom.xml的dependencies中加入以下内容:

```xml
<dependency>
    <groupId>cn.hutool</groupId>
    <artifactId>hutool-all</artifactId>
    <version>5.3.2</version>
</dependency>
```

## Gradle
```
compile 'cn.hutool:hutool-all:5.3.2'
```

## 非Maven项目

点击以下任一链接，下载`hutool-all-X.X.X.jar`即可：

- [Maven中央库1](https://repo1.maven.org/maven2/cn/hutool/hutool-all/5.3.2/)
- [Maven中央库2](http://repo2.maven.org/maven2/cn/hutool/hutool-all/5.3.2/)

> 注意
> Hutool 5.x支持JDK8+，对Android平台没有测试，不能保证所有工具类或工具方法可用。
> 如果你的项目使用JDK7，请使用Hutool 4.x版本

### 编译安装

访问Hutool的码云主页：[https://gitee.com/loolly/hutool](https://gitee.com/loolly/hutool) 下载整个项目源码（v5-master或v5-dev分支都可）然后进入Hutool项目目录执行：

```sh
./hutool.sh install
```

然后就可以使用Maven引入了。


