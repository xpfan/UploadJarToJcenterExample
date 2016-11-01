# UploadJarToJcenterExample
Upload Jar To Jcenter Example
1、首先，下载本项目。
      方式一：Use Git or checkout with SVN using the web URL;检出后导入到android studio项目中。
      方式二：download zip;解压导入android studio项目中。
2、其次，你需要到https://bintray.com/注册账号。
注：注册的时候可以用第三方的账号直接登录github账号、google账号。（如果你第三方的账号邮箱是qq、163好像不行；本人试过不行。）
       当然，如果你要自己注册，这里会有一个坑，qq、163的邮箱注册不了，验证会一直报邮箱有问题（本人试过不行）。
       后来我注册了一个hotmail邮箱，再注册bintry的账号就成功了。
3、注册完好了之后，再创建仓库。点击 Add New Repository链接创建仓库，记住Type选择Maven(这里是Maven),仓库名字可以自己命名。
      注释：创建完了之后你可以手动添加包名；这里我们不用手动创建，我们使用Gradle项目去自动构建包名并上传到bintray上。
5、仓库创建好之后，首先去获取API KEY.
      步骤：右上角个人头像下拉菜单中点击“ManageOrganizations”,页面出来后，点击左侧导航菜单中会看到一个叫“API KEY”的菜单，获取API KEY.
6、在Android Studio项目中的local.properties文件中加入两行配置
	bintray.user=bintray的用户名
	bintray.apikey=bintray获取的API KEY
7、以上都OK了之后，修改mylibrary模块下的build.gradle配置，将相应的配置修改为自己的配置。详细配置请见build.gradle配置文件中相应说明。

8、所有步骤都OK了之后，就可以开始上传library了。
步骤：
1、打包（准备上传要使用的包）:命令：gradlew install
2、打包成功之后使用上传命令：gradlew bintrayUpload

9、步骤8都显示成功了之后，说明已经传到bintray上了；这个时候你就可以到之前创建的仓库中去查看上传的package了。
       
10、同步到JCenter(Maven中央仓库，其他人就可以使用了)。
        首先进入package详情，点击右下角会看到一个叫"Add To JCenter"。按照步骤填写Group Id（group id填写成你打包时的group即可，保证唯一，本例是“com.example.xpfan.grpc”）和备注。点击“Send”按钮。
        接下来就是等待审核通过就可以用了。
 
       说明：这里我等了很久都看不到package链接到 Jcenter。但我还是可以引用package；当我晚一点登录的时候才看到已同步到JCenter，可能是网址数据同步的问题（毕竟人家是大数据网址嘛）。

附：可验证本项目自身已上传的library
maven:

<dependency>
  <groupId>com.example.xpfan.grpc</groupId>
  <artifactId>mylibrary</artifactId>
  <version>1.0.0</version>
  <type>pom</type>
</dependency>

gradle:

compile 'com.example.xpfan.grpc:mylibrary:1.0.0'

Ivy:
<dependency org='com.example.xpfan.grpc' name='mylibrary' rev='1.0.0'>
  <artifact name='$AID' ext='pom'></artifact>
</dependency>

步骤如有遗漏，请发邮件到46273600@qq.com 指正，一起交流。