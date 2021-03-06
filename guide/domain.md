

# 域名管理

## 测试域名

对象存储空间默认提供测试域名进行访问。默认该测试域名关闭。  
当您没有自己的域名创建CDN加速时，可以点击开启一键创建CDN加速域名试用。  
测试域名是由我们系统完成备案和配置CNAME至UFile对应存储空间域名。有关测试域名的CDN高级配置，请到[UCDN产品页](https://console.ucloud.cn/ucdn/ucdndomainmanage)进行操作。  
使用此CDN加速域名访问将产生CDN流量和CDN回源流量费用，流量费用请参照[UCDN计费规则](https://docs.ucloud.cn/cdn/ucdn/charge)。  
![](/images/guide/测试域名v4.png)

## 自定义域名

实际生产环境推荐您绑定自定义域名创建CDN加速。自定义域名的操作，请按照以下步骤进行：

**单地域空间管理**

1、确认自定义域名已经完成备案（若未进行备案，域名会被管局停止解析，导致业务不可用），备案相关请
[参考这里](https://beian.ucloud.cn)。

2、UFile控制台提供管理自定义域名功能，用户可操作绑定自定义域名并开启加速。  
选择对应空间，在右侧的操作中点击域名管理按钮。

![](/images/guide/点击域名管理v4.png)

在自定义域名弹窗中输入需要绑定的自定义域名，选择是否CDN加速。

![](/images/guide/绑定自定义域名弹窗v4.png)

CDN加速选项在UCDN产品页加速和管理，选择CDN加速为"是"，点击确定后将前往UCDN产品页面继续完成操作。
![](/images/guide/绑定加速域名v4.png)

跳转到UCDN产品页面继续完成基础配置和高级配置。 ![](/storage_cdn/ufile/guide/跳转到cdn创建界面v4.png)
