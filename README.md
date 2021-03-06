<!--
 * @Descripttion:
 * @version:
 * @Author: xiaowu
 * @Date: 2020-03-05 10:12:57
 * @LastEditors: xiaowu
 * @LastEditTime: 2020-03-05 14:37:24
 -->
# web_crawler 网络爬虫
# 基于node的爬虫
`作者：xiaowu`
# 功能
### 1.可以将指定的页面，指定的相同结构的数据爬取下来，成为接口在线使用
### 2.可以根据域名的规律，使用get请求，通过传入不同的id来获取相同结构的不同页面的数据
### 3.可以将爬取到的数据保存为文件，用来存入数据库或长期保存
### 4.已做跨域设置，端口号默认3003，服务器已测试可用

# 使用场景
###### **1.可以直接部署到线上服务器上，通过访问自己服务器的接口，自己服务器去目标页面取到数据后由返回给自己的服务器（白嫖数据）**
###### **2.抓取目标的数据，保存到文件，用以备份，长期存储，或存储到自己的服务器上**
###### **3.学习或开发没有数据，爬到数据用于学习和测试**
###### **4.测试自己的网站防爬虫功能是否完善**


***
###### **页面默认返回json数据**

***

[线上接口测试1](http://47.95.9.203:3003/)

**效果图片**
![线上测试一](https://github.com/xiaowu2333/web_crawler/blob/master/img/test1.png)

***
[线上接口测试2](http://47.95.9.203:3003/data?id=186900)

**效果图片**
![线上测试二](https://github.com/xiaowu2333/web_crawler/blob/master/img/test2.png)

***

**控制台效果图**
![控制台效果图](https://github.com/xiaowu2333/web_crawler/blob/master/img/test3.png)




***

# 使用方法：

### 1 安装依赖
`npm i`

### 2 使用pm2/node 挂载index.js

`node index.js`


# 注意：

#### 如果想要存到文件,把注释的代码打开。

#### 如果要爬需要cookie验证的网站
`写法:`

```
//可以用set设置cookie
//网页的cookie可以通过控制台 document.cookie获取
 let cookie = "这里是cookie"
 superagent.get(url).set("Cookie",cookie).end()
```

#### 如果需要爬带有header验证的网站
`写法：`
```
//可以用set设置头部信息
request.get('/search').set('API-Key', 'foobar').set('Accept', 'application/json');
```


`注：仅供学习使用，不得做他用`