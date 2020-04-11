# 会话技术

* **会话的概念**：一次会话中包含多次请求与响应
  * 一次会话：浏览器第一次给服务器资源发送请求，会话建立，直到有一方断开为止
* **功能：** 在一次会话的范围内的多次请求中共享数据
* **方式：**Cookie（客户端）、session（服务端）

## 1. Cookie

1. 概念：客户端会话技术，将数据保存到客户端。

2. 使用步骤：

   * 创建Cookie对象，绑定数据
     * new Cookie(String name,Object value)
   * 发送Cookie对象
     * response.addCookie(Cookie cookie)
   * 获取Cookie，拿到数据
     * request.getCookies()

3. 实现原理

   * 基于响应头set-cookie和请求头cookie实现

4. 细节

   * 一次可不可以发送多个cookie

     * 可以

   * cookie在浏览器中保存多长时间

     	* 默认   浏览器关闭，则销毁cookie
      * 设置cookie的生命周期
        * setMaxAge（int  seconds）
          1. 正数：将cookie数据写入硬盘的文件中，持久化存储。cookie的存活时间
          2. 负数：默认值
          3. 零：删除cookie的信息

   * cookie获取的范围有多大

     * 假设在一个tomcat中部署了多个web项目，那么这些web项目中cookie能不能共享？
       * 默认情况下不能共享
       * setPath（String path）  ：设置共享范围
       * 如果要共享，可以设置为“/“
     * 不同tomcat服务器cookie共享问题
       * setDomain(String path):如果设置一级域名相同，那么多个服务器之间cookie可以共享

   * cookie可不可以存中文

     Tomcat8.0之后可以直接使用中文

5. Cookie的特点和作用

   * cookie存储数据在客户端和浏览器
   * 浏览器对于单个cookie的大小有限制（4KB)以及同一域名下的总cookie数量也有限制
   * 作用：
     1. cookie一般用于存储少量不敏感的数据
     2. 在不登录的情况下，完成服务器对客户端的身份识别

6. 案例

   * 记住上一次访问时间

   * 需求：访问一个servlet ，如果第一次访问，则提示：你好，欢迎首次访问

     ​				如果不是，提示：显示时间字符串



## 2. Session

----

#  复习

setPath（）

setMaxAge()