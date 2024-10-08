# 更新日志

## 2024-09-13
01. 此次为重大更新，重写整体框架，将框架路由和模块重新更新，整体架构更清晰

## 2024-03-27
01. 添加了一些常用的小工具 ，判断手机请求，post,get,options等请求 封装为函数内置小工具
 
## 2024-03-01
01. 添加JsonDB类 ，可以更加方便的操作JSON文件 或者可以理解为本地文件数据库
02. 优化网址URL显示格式，常量为：PG_URL_EXPLODE
03. 优化u()函数 和 url() 函数生成的网址格式保持和 网址显示格式一致
04. 增加t()函数，方便new 工具库类，方便不需要构造函数时候加载工具类使用
05. 重新优化支付宝几种支付方式类（当面付不建议用异步方式，使用轮询比较方便）
## 2024-01-18
01. 添加模块配置功能 某个具体模块的配置数据，比如 文章模块 : 每页展示数量、文章状态等，作用于某个具体模块；
02. 支持使用composer(框架已集成composer)添加类库
03. 添加Swiftmailer发送邮件类库安装和调用(框架已集成)
04. 优化常量 , 重写文件型缓存

## 2021-04-25
kouGrace 自 2021年4月25日停止更新及闭源    
框架并无致命 BUG，停更核心原因是无法控制框架使用者会不会使用框架做”违法”的坏事。    
感谢大家的一路相伴，也谢谢大家的谅解 ~

## 2020-07-23
01. 添加 自定义缓存类文件支持，提升缓存的复用能力 查看手册;;
02. 优化 memcache 形式的缓存类，优先调用 memcached 类;

## 2020-07-20
01. 添加控制器类自动加载功能，从而支持控制器内调用其他的控制器;
02. 添加控制器调用演示代码, 查看手册;
03. 提供应用基础目录结构建议，包含 : 网站前端、管理后台、api接口;

## 2020-07-20
01. 优化框架核心文件结构，将常用函数封装到 graceFunctions.php;
02. 框架注释全面优化，阅读源码更友好;
03. 新增追踪信息，展示运行信息、文件信息、sql 语句三个模块，对开发更友好;
04. 优化错误及异常处理机制;
05. 更新全局配置文件创建规则，以便于之后的框架可以实现无缝升级;