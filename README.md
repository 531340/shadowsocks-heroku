shadowsocks-heroku
==================

shadowsocks-heroku is a lightweight tunnel proxy which can help you get through firewalls. It is a port of [shadowsocks](https://github.com/clowwindy/shadowsocks), but through a different protocol.

shadowsocks-heroku uses WebSocket instead of raw sockets, so it can be deployed on [Heroku](https://www.heroku.com/).

Notice that the protocol is INCOMPATIBLE with the origin shadowsocks.

Heroku
------
仅供学习，后果自负 https://www.heroku.com/policy/aup

 [![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/neroku/shadowsocks-heroku/tree/heroku-test)
  
客户端 https://github.com/v2ray/v2ray-core/releases

```
"outbound": {
		"protocol": "shadowsocks",
		"settings": {
			"servers": [{
				"address": "neroku.herokuapp.com",
				"port": 80,
				"method": "aes-256-cfb",
				"password": "justest",
				"ota": false
			}]
		},
		"mux": {
			"enabled": false
		},
		"streamSettings": {
			"network": "ws"
		}
	},
```

Supported Ciphers
-----------------
- aes-128-cfb
- aes-256-cfb

