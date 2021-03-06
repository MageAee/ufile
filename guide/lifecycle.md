

# 生命周期

您可以通过开通存储空间（Bucket）生命周期功能，实现存储空间内所有文件或特定前缀文件的生命周期管理（可以配置一个或者多个规则），设置生命周期规则进行归档存储或删除文件操作。

* 删除文件：支持设置指定的文件在 N 天后被自动删除。

## 使用场景

通过生命周期规则，您可以更高效的管理您存储的数据，节省大量人力及存储成本。您可以通过设置匹配特定前缀的规则，定期将不再需要访问的数据删除。

## 注意事项

1. 存储空间的生命周期功能一旦开启，对存储空间内所有符合规则范围的文件生效（包括开启生命周期功能前上传的文件），并于后一天的00:00触发生命周期规则，请确认无误后再保存生命周期规则。

2. 删除文件的操作是不可逆的，请根据您的需求合理设置生命周期规则，避免重要数据丢失。

## 管理生命周期

选择对应空间，在右侧操作中选择生命周期按钮。

![](/images/guide/进入生命周期管理界面.png)

点击添加规则按钮。

![](/images/guide/生命周期管理界面.png)

添加生命周期规则界面。

![](/images/guide/添加生命周期规则.png)

1. 规则名称：用户可以设置一个规则名称，记录自己创建的规则。

2. 规则范围：指定规则的生效范围，选择整个存储空间时，生命周期规则对整个存储空间生效，选择指定目录时，仅对该存储空间下的指定目录生效。

3. 规则内容：选择规则的触发时间，最小为 7 天，具体计算方式请参考备注说明。

生命周期规则添加完成后默认生效，生效状态具体可见状态栏，您可以通过操作栏下的其他按钮，进行相应的修改以及关闭操作。

![](/images/guide/查看生命周期规则状态.png)

点击禁用或者删除按钮以后，状态修改在第二天生效，不影响当天00:00已触发但未执行完成的任务继续执行。

### 备注

1. 低频存储和归档存储类型都有最短存储期限，早于最短存储期限删除、修改、覆盖文件，需要补足未满最短存储期限的剩余天数的存储费用。

2. 生命周期规则的自动操作触发时间是如何计算的呢？UFile将文件上传时间与设置天数相加，计算得到时间的后一天的00:00（CST: 中国标准时间）即为自动操作开始时间。例如文件在2015年1月1日上午10:00 CST上传，设置在 3 天后被删除，那么会在2015年1月5日00:00 CST后触发自动删除文件操作。

3. 当前仅北京、广州、上海二地域支持生命周期功能，其他地域后续支持。
