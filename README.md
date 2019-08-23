# Server-sent events

Server-sent events implementation in Go.

It allows **unidirectional** communication from an HTTP server to a webpage.

- [Living Standard](https://html.spec.whatwg.org/multipage/server-sent-events.html)
- [Browser support](http://caniuse.com/#feat=eventsource)

## Why?

Because I find the existing libraries are not very Go-like, more like ports from another language.

## Considerations

- `Content-Type` header is forced to `text/event-stream;charset=utf-8`.
- It works as an `io.Writer` and takes data from an `io.Reader`, no assumptions made over it.
- It's a new library, you might be looking for a more battle-tested implementation like:
	- [gin-contrib/sse](https://github.com/gin-contrib/sse)
	- [manucorporat/sse](https://github.com/manucorporat/sse)

