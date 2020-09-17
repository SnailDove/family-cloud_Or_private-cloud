# family-cloud_Or_private-cloud

结合低功耗x86主机，再借助Unraid虚拟机系统搭建家庭服务器。

## 目标：

具备如下功能：
1. 家庭数据 ：私有云——大小取决于装了多大硬盘，后期随意升级，上传下载速度取决于你的带宽（目前国内三大运营商手机套餐：移动88元/月，电信联通99~100多元/月——这些套餐赠送的宽带下行100Mb/s=12.5MB/s 上行50Mb/s=6.25MB/s），在线网络硬盘可在线编辑，随时同步文档（各种定制化的配置文件，比如：vim）、照片/视频（可自动生成时间线）、私有代码仓库、博客服务器；省去随身携带的u盘、硬盘，以及解决手机电脑存储不够用的麻烦。

2. 多媒体中心：在线4k高码率硬件解码+推流，客户端随时查看私有云里面的音视频，只要有浏览器和网络均可播放，已具备免费：安卓、ios、windows、Mac客户端。没有网络情况下，局域网内，可推送音视频到任何一台设备；可根据链接、种子远程挂载下载任务，一地下载随时随地多设备访问。

3. 高性能软路由：配合VPN，实现高速访问外网，可实时观看油管/Plex 4k60Hz 视频。

注：不限制用户数，文件夹可设置访问权限。体验取决于同一时间使用的用户数以及带宽的上行速度。

## x86低功耗机器配置
| 项目   | 型号                                                         | 价格，单位：元                            |
| :----- | :----------------------------------------------------------- | ----------------------------------------- |
| CPU    | G5620 TDP: 54W 2c4t 基频:4GHz UHD630：4k h265解码 100Mbps<br/>备选：G6400 性能一样， 价格一样，区别1200接口，散片与上价格一样 | 345 散片                                  |
| 主板   | MSI B360m 迫击炮——1151接口日后可升级8/9代性能更高的CPU, Sata3: 6个硬盘位，PCIEx1 2个：可扩展万兆网口和磁盘阵列卡，PCIEx16 2个口：可扩展eGPU，2个m2，第二个m2与第二个PCIEx16冲突，如果日后想黑苹果，github上完善的EFI很多。<br/>备选：MSI B460m 迫击炮 与b360迫击炮优点点：2.5G有线网卡，1200接口，兼容下一代处理器，如果日后黑苹果，github上完善的EFI很多；缺点：价格770元。<br/>**注意**：主板不买二手，因为7x24小时不间断工作，二手主板怕电容老旧和缺陷，比如电压不稳进而不久就损坏甚至造成起火爆炸，殃及硬盘数据，因此这一块不想冒险。 | JD全新550（二手350元，咸鱼未拆封：480元） |
| 内存   | 光威奕pro DDR4 8g 2666/3000 单条，毕竟NAS性能不挑，只要够大  | 拼多多百亿补贴：160                       |
| 固态   | Sata3 240g作为机械硬盘缓存盘，提高体验；<br/>可升级体验：m2协议固态，这样提升日常访问网络硬盘当中小文件的速度，比如office三件套、markdown文档、配置文件等等。 | ~~150 京东全新~~（已有）                  |
| 网卡   | 主板自带有线网卡；<br/>可升级：PCIE转双口千兆。              | --                                        |
| 机箱   | 爱国者nas机箱，自带4个3.5、2个2.5盘位，光驱位可扩展2个3.5寸盘位，总共：6个3.5寸硬盘盘位+2个2.5寸盘位+主板自带双m2插槽，家庭使用够用了。 | 150 顺丰包邮                              |
| 电源   | 鑫谷（Segotep）额定500W GP600G黑金全模组电源，5年质保；<br/>**注意**： 由于7x24小时不间断工作，所以尽量买好的电源，防止供电不稳损坏硬盘甚至造成主板爆炸，进而殃及池鱼，最后数据丢失，因此这一块不想冒险。 | 360 全新                                  |
| 散热   | intel cpu原装风扇 +3个风扇                                   | 15 2手 + 10 全新                          |
| 数据线 | 山泽 SATA3 数据线 9元 *  4<br/>**注意**：由于硬盘7x24小时不间断工作，防止数据线品质不好，比如电压不稳造成硬盘损坏，进而丢失数据，因此这一块不想冒险。 | 35                                        |
| 总计   |                                                              | 1625                                      |



