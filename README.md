# ctjs-multiplayer
#Connectivity
* Websocket
* XHR-polling

**Websocket**

Websocket is the obvious choice when it comes to raw performance

**XHR**

Xhr is a older protocol built on http1,each packet is sending  3 HTTP requests per request

**Performmance**

By default websockets is 10x more performant than polling but the downside to that is that some users may not be able to connect directly to a websocket server due to network settings ie vpn,admin settings,firewalls etc.
Instead of asking users to disable those things the best approach is to utilize something that's a hybrid between the two

**Engine.io**

Engine.io is a abstraction above Websockets that makes connectivity its number 1 priority,If it detects that the client cant use websockets due to a issue it auto routes to long polling,if it detects websocket is supported and not blocked it upgrades to websockets

**Conclusion**

This will be built utilizing Engine.io due to the reliability the abstraction brings over just using websockets
