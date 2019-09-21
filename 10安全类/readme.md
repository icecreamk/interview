- CSRF（Cross-site request forgery）跨站请求伪造
    + 攻击原理
        * 用户在网站A登录成功之后，A网站返回cookie存储在本地。用户访问B网站时候，恶意链接诱使用户通过攻击者的链接提交请求给相关接口(cookie会自动携带)
    + 防御措施
        * 添加Token验证（Token不会自动携带）
        * Referer验证（页面来源验证）
        * 隐藏令牌（隐藏在http头中，不会放在链接上）
- XSS（Cross-site scripting） 跨域脚本攻击
    + 原理
        * 在页面注入恶意脚本
    + 防御措施
        * 使XSS脚本不可执行