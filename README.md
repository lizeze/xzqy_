# 简介

全国行政区域json文件， 包括省，市，区，县，镇，街道

数据持续更新中。。。

# 保存目录

```
data
│  ├─1  
│  ├─2
│  ├─3
│  └─4
```

* 1 省
* 2 市
* 3 区/县
* 4 镇/街道

根据层级结构保存在不同的文件夹中，文件的命名都是上级区域的id。

 比如北京的`id`是110000,那么海淀区所在的文件名称就是`110000.json` 以此类推

 # 启动项目

  下载代码到本机
  ```shell
  $ git clone https://github.com/lizeze/china_region.git
  ```
  安装依赖

  ```shell
   $ cd china_region
   $ npm i 
   $ npm start
  ```
  Get `http://localhost:9600/v1/api/xzhf/fid=100000&level=1`

  |     |   |
|  ----  | ----  |
| level  | 请求的数据类型，和保存目录一致 |
| fid  | 请求数据的父节点 |
# 生成sql文件

``` 
 $ npm run sql     #全部数据生成sql

 $ npm run sql 1   #生成省级sql

 $ npm run sql 2   #生成市级sql

 $ npm run sql 3   #生成县级sql

 $ npm run sql 4   #生成街道sql

```

修改`sql`字段名称

`./src/tool.js`
 ``` javascript
 let sqlObj = {
    tableName: 'table1',
    id: 'id',
    name: 'name',
    level: 'level',
    parent: 'parent',
};
 ```

 # 历史

  * 2020-10-31
  
    增加廊坊，沧州，承德街道数据
  * 2020-11-01
    
     增加 晋中，吕梁,运城，临汾,长治街道数据
  * 2020-11-02
  
     增加 新疆维吾尔自治区街道数据
   * 2020-11-02
  
     增加 内蒙古自治区街道数据
   * 2020-11-03

      增加 内蒙古自治区街道数据

      增加生成sql语法方法  
    * 2020-11-04

      增加 江苏街道数据

     
    
