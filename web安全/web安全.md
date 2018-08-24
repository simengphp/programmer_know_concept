##web安全的相关概念总结

（1）CSRF（cross-site request forgery）跨站请求伪造
方法：劫持cookie或者sessionid
解决：每次请求加入token

（2）XSS（cross site script） 跨站脚本攻击
方法：提交一些脚本信息<script>alert('1')</script>
解决：过滤用户提交的信息，将html标签转成实体

（3）session攻击，会话劫持
方法：获取到用户的sessionID
解决：每次登陆重置sessionid，设置HTTPOnly,防止客户端脚本访问cookie信息，组织xss攻击
关闭透明化sessionid，user-agent头信息验证，token验证

