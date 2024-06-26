# Websocket 协议的相关知识

## 1. Websocket 协议简介

Websocket 是一种在单个TCP连接上进行全双工通信的协议，它使得数据可以从服务器端到达客户端，也可以从客户端传送到服务器端。Websocket 协议使得客户端和服务器之间的数据交换变得简单，允许服务端主动向客户端推送数据。

## 2. Websocket 协议的特性

- 全双工通信：在Websocket 上，客户端和服务器都可以主动发送或接收数据。
- 实时性：由于协议是全双工的，服务器可以随时主动给客户端下发数据。在Websocket 出现之前，我们只能使用轮询的方式，让客户端定时向服务器发出请求，看是否有新的信息。
- 保持连接状态：与HTTP不同的是，Websocket 需要先创建连接，然后才能进行全双工通信。
- 更好的性能：Websocket 是直接基于TCP的，不存在大量的HTTP的包头信息，从而减少数据传送的延迟。

## 3. Websocket 协议的工作流程

Websocket 的工作流程可以分为两个阶段：握手阶段和数据传输阶段。

1. 握手阶段：在此阶段中，客户端和服务器会通过HTTP协议进行握手。如果握手成功，协议升级从HTTP协议切换为Websocket 协议，此后的通讯就直接通过TCP协议进行数据传输。
2. 数据传输阶段：握手阶段完成后，客户端和服务器就可以任意地双向通信了。

## 4. Websocket 协议与HTTP协议的区别

- 连接方式：HTTP 是无状态的，每次请求都需要建立新的连接；而Websocket 在建立连接后，就可以进行任意次的双向数据传输。
- 数据传输性能：HTTP协议的头信息比较多，对于小数据量的传输，效率较低；而 Websocket 的头信息相对较少，对于实时性要求较高的场景（例如聊天、在线游戏等），Websocket 更具优势。

## 5. Websocket 在微信小程序中的应用

微信小程序提供了对Websocket 的原生支持。在微信小程序中，可以使用wx.connectSocket()方法创建一个Websocket 连接。同时，微信小程序还提供了一系列的API，如wx.onSocketOpen()、wx.onSocketMessage()、wx.sendSocketMessage()、wx.closeSocket()等，用于管理Websocket 连接的生命周期和处理Websocket 的各种事件。

## 结论

Websocket 协议为构建实时应用提供了强大的支持。了解和掌握Websocket 协议，对于进行微信小程序开发，尤其是需要实时数据交换的场景，非常重要。
