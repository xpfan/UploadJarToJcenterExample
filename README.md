# UploadJarToJcenterExample
Upload Jar To Jcenter Example
1�����ȣ����ر���Ŀ��
      ��ʽһ��Use Git or checkout with SVN using the web URL;������뵽android studio��Ŀ�С�
      ��ʽ����download zip;��ѹ����android studio��Ŀ�С�
2����Σ�����Ҫ��https://bintray.com/ע���˺š�
ע��ע���ʱ������õ��������˺�ֱ�ӵ�¼github�˺š�google�˺š����������������˺�������qq��163�����У������Թ����С���
       ��Ȼ�������Ҫ�Լ�ע�ᣬ�������һ���ӣ�qq��163������ע�᲻�ˣ���֤��һֱ�����������⣨�����Թ����У���
       ������ע����һ��hotmail���䣬��ע��bintry���˺žͳɹ��ˡ�
3��ע�������֮���ٴ����ֿ⡣��� Add New Repository���Ӵ����ֿ⣬��סTypeѡ��Maven(������Maven),�ֿ����ֿ����Լ�������
      ע�ͣ���������֮��������ֶ���Ӱ������������ǲ����ֶ�����������ʹ��Gradle��Ŀȥ�Զ������������ϴ���bintray�ϡ�
5���ֿⴴ����֮������ȥ��ȡAPI KEY.
      ���裺���ϽǸ���ͷ�������˵��е����ManageOrganizations��,ҳ������󣬵����ർ���˵��лῴ��һ���С�API KEY���Ĳ˵�����ȡAPI KEY.
6����Android Studio��Ŀ�е�local.properties�ļ��м�����������
	bintray.user=bintray���û���
	bintray.apikey=bintray��ȡ��API KEY
7�����϶�OK��֮���޸�mylibraryģ���µ�build.gradle���ã�����Ӧ�������޸�Ϊ�Լ������á���ϸ�������build.gradle�����ļ�����Ӧ˵����

��������֤����Ŀ�������ϴ���library
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

����������©���뷢�ʼ���46273600@qq.com ָ����һ������