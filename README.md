To add packages append
```
src-git jaka https://github.com/jaka/opkg-packages.git
```
or
```
echo "src-git jaka https://github.com/jaka/opkg-packages.git" >> feeds.conf
```
to `feeds.conf.default` in buildroot directory and run
```
./scripts/feeds update
./scripts/feeds install -a
```
