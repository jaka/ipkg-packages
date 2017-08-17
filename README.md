To add packages append
```
src-git jaka https://github.com/jaka/opkg-packages.git
```
to `feeds.conf.default` in buildroot directory and run
```
./scripts/feeds update
./scripts/feeds install -a
```
