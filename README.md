# forcedata-packages-luci
luci for forcedata-packages-luci

## 使用方法

### 增加feed源

```shell
echo >> feeds.conf.default
echo 'src-git forcedata https://github.com/hequan2017/forcedata-packages-luci' >> feeds.conf.default
./scripts/feeds update  forcedata
./scripts/feeds install -a -p forcedata
```

### 集成软件包

```shell
make menuconfig
```

选择软件包
```plain
LuCI --->
3. Applications --->
<*> luci-app-forcedata................................. LuCI support for forcedata
```


### 构建固件
```shell
make
```