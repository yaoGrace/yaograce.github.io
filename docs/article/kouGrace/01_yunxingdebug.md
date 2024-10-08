# 运行 · 调试

## 运行流程
kouGrace 框架运行流程 : 
01. http 请求， 如 : http://www.xxxx.com/index 
02. 服务器伪静态规则将请求统一重定向到入口页面 index.php  ；
03. 框架核心文件初始化运行；
04. 路由解析 : 运行解析规则对应的控制器及方法，并解析保存其他 url 参数；
05. 调用缓存、模型、工具、视图等完成某个具有页面的运行工作；

## 框架调试
kouGrace 内置了调试功能，可以在运行页面展示一下调试信息 :

01. 当前请求服务器运行时间、消耗内存数量；
02. 当前请求执行过程中引用的所有文件；
03. sql 运行日志，包含 : sql 语句、查询时间、错误信息；

## 关闭调试

一旦开发完毕，并将项目部署至服务器，就应该关闭调试功能  
关闭方法 :  
打开对应分组下的入口文件 : /index.php   
```php

// 是否调试或者404页面  
//开发环境(debug调试 跳转到默认模块-默认控制器-默认方法)-false 
//正式上线后(错误就404页面)-true
const KG_ERROR_404_PAGE = false;

// 是否开启追踪模式 默认为 false - 关闭, true - 开启
const KG_TRACE = false;
```
::: warning 注意事项
调试会在请求页面直接展示调试所需的 html 结果，如果您开发的是应用 api 接口请关闭调试，避免调试内容影响接口请求数据。
:::

**错误展示**  
kouGrace 重构了 php 的错误展示，以较为清晰的方式来展示代码错误及异常；
 