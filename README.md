# WebSocket proto file

For now BigONE's [spot websocket api](https://open.big.one/docs/spot_pusher.html) supports the `proto` protcol.

With [Protocol Buffers](https://developers.google.com/protocol-buffers), you can get many benefits:
* message size is 10 times smaller than the json format.
* faster decoding.
* less memory usage.
* Strong typing.

You can receive the messages faster as the message body is much more smaller.

## How to use

Just set the `Sec-WebSocket-Protocol` header to `proto`.

Then sever will send you [binary messages](https://tools.ietf.org/html/rfc6455#section-5.6), and you should decode them with the `websocket.proto` file.
