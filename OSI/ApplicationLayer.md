# ApplicationLayer

常见的应用层协议：

- HTTP
- HTTPS
- FTP
- SMB

## HTTP
> HyperText Transfer Protocol

HTTP 协议已经演进了很多版本，大部分是向下兼容的，[RFC 2145](https://tools.ietf.org/html/rfc2145) 描述了 HTTP版本号用法。

### HTTP/1.1

#### URL

`HTTP URL` 包含了用于查找某个资源的详细信息, 格式如下:
```text
http://host[":"port][abs_path]
```

#### 请求

<table>
    <tr>
        <td>Method</td>
        <td>Request-URI</td>
        <td>HTTP-Version</td>
        <td>CRLF</td>
    </tr>
    <tr><td colspan="4">消息报头</td></tr>
    <tr><td colspan="4">空行 (只有CRLF的行)</td></tr>
    <tr><td colspan="4">请求消息体(可选)</td></tr>
</table>

#### 请求状态行

> 请求行由请求Method, URL 字段和HTTP Version三部分构成, 总的来说请求行就是定义了本次请求的请求方式, 请求的地址, 以及所遵循的HTTP协议版本例如：

```text
GET /index.html HTTP/1.1 (CRLF)
```

请求方法：

- GET
- POST
- PUT
- DELETE
- OPTIONS
- HEAD
- TRACE
- CONNECT
- PATCH

#### 请求头

Header 由 Key Value 组成，每行为一个 Header。

- `Accept: text/plain`
- `Content-Type: application/octet-stream`

#### 请求消息体

message body 可以是一行字符串。例如：下面的 `Hello world!`

```text
HTTP/1.1 200 OK
Accept-Ranges: bytes
Content-Length: 12
Connection: close
Content-Type: text/html

Hello world!
```

#### 响应

<table>
    <tr>
        <td>HTTP-Version</td>
        <td>Status-Code</td>
        <td>Reason-Message</td>
        <td>CRLF</td>
    </tr>
    <tr><td colspan="4">消息报头</td></tr>
    <tr><td colspan="4">空行 (只有CRLF的行)</td></tr>
    <tr><td colspan="4">响应消息体(可选)</td></tr>
</table>

#### 响应状态行

```text
HTTP/1.1 200 OK （CRLF）
```

#### 响应状态码
> 可参考 [List of HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)

- 信息 `1XX`
- 成功 `2XX`
- 重定向 `3XX`
- 客户端错误 `4XX`
- 服务端错误 `5XX`

#### 响应消息体

响应体 通常是一段 HTML （在Header 里 有声明 `Content-Type: text/html;`）。像是这样：

```text
HTTP/1.1 200 OK
Content-Type: text/html; charset=UTF-8
Content-Length: 155
Accept-Ranges: bytes
Connection: close

<html>
  <head>
    <title>An Example Page</title>
  </head>
  <body>
    <p>Hello World, this is a very simple HTML document.</p>
  </body>
</html>
```

### HTTP/2

### HTTP/3

## HTTPS

## 参考文献
- [深入理解HTTP协议](https://zhuanlan.zhihu.com/p/45173862)
- [Hypertext Transfer Protocol](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
- [超文本传输协议](https://zh.wikipedia.org/wiki/%E8%B6%85%E6%96%87%E6%9C%AC%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE)
- [HTTP/2](https://zh.wikipedia.org/wiki/HTTP/2)
