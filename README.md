**项目简介：**

- 项目名称：科协纳新报名系统
- 服务端：CentOS 7.0_64位 + Tomcat
- 数据库：MySQL
- 编程语言：Java
- 应用技术：JavaBean + JDBC + Servlet + Jsp

总共加起来大概得有5天的时间吧，一直在做着科协的纳新报名系统，现在，总算大功告成了，记录一下我的第一个上线项目的开发历程。

第一次做真实项目，感觉和平时的小打小闹还是有很大不同的。平时做的项目，只要目标功能实现了就行，不必考虑过多的其他问题，如浏览器兼容问题、数据格式规范化问题等，可当一个项目真正投入使用，这些问题都必须得考虑并解决。

该项目虽然功能很简单，但是自我感觉“麻雀虽小，五脏俱全”（也可能是自己家的“孩子”，所以觉得亲吧）。现将该项目相关信息总结如下：

**涉及到的相关知识点：**

1. SmartUpload文件上传下载插件
2. Bootstrap——用于前端页面设计，主要为实现网站自适应功能。（PS：前端由老曹童鞋负责，我只是打酱油的）
3. Ajax——用于判断学号在数据库是否已存在
4. Servlet过滤器——用于设置编码格式
5. Log4j——项目日志
6. 防重复提交
7. 在web.xml中配置错误跳转，提高网页的友好性
8. 正则表达式、获取上传文件的大小和格式——将前端获取的数据格式规范化
9. 使用SSH工具在Linux系统中远程部署web工程

**经验与总结：**

- 在前端对提交的数据进行规范化判断，这样既方便后台功能的开发和逻辑处理，又能提高用户的体验（使用中基本不会弹出错误页面）
- 在Servlet页面尽量不要直接输出提示信息，易出现乱码问题
- 用**$("#id").is(":checked")**判断单/复选框是否被选中，取值为false或true，id为单/复选框的id
- 保存数据后，左下角会有“正在提交”一直在运行，只有刷新页面才能制止它
- 使用Ajax时，$.ajax中的dataType:'json'可以考虑删除，否则对传递的数据的格式要求过于严格

又学到一招：微信和百度浏览器使用IP访问网页的话，每次跳转都会被拦截下来，导致数据无法提交！
