##### 如编译失败，搜索RAW日志中的
```
Collected errors
```
##### 软件包之间的冲突:
1. luci-app-systools / luci-app-netspeedtest 与 speedtestcli 冲突
2. luci-app-socat 与 socat 冲突
关闭其中之一即可，因为makefile中已声明依赖关系，无须重复单独安装。主要原因是，两个不同的feed源同时标注了同样的包安装，且其中重复的这个软件包（假设为B）又和另一个软件包（假设为A）存在依赖关系，且这个相互依赖的包在编译过程中已经被安装了，如果再执行一次单独的B安装，就会提示冲突。

##### 更新:
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/grayearth/BuildAuto?style=for-the-badge&logo=appveyor&label=最新固件)](https://github.com/grayearth/BuildAuto/releases/latest)


#### 注意：
本项目是**自用**项目，如直接使用可能与你所使用的环境并不相符，会引起不必要的麻烦，请谨慎借鉴。


## License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
