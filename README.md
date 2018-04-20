To add packages append
```
src-git jaka https://github.com/jaka/opkg-packages.git
```
to `feeds.conf`, or execute
```
echo "src-git jaka https://github.com/jaka/opkg-packages.git" >> feeds.conf
```
in buildroot (source) directory and update feeds by running
```
./scripts/feeds update
./scripts/feeds install -a
```
Then enable packages in `make menuconfig`.
