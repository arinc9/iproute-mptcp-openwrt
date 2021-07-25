Add iproute-mptcp feed to the bottom of `feeds.conf.default`:
```
src-git iproutemptcp https://github.com/arinc9/iproute-mptcp-openwrt.git
```

Refresh feeds and install iproute-mptcp feed
```
./scripts/feeds update -a && ./scripts/feeds install -a
```
