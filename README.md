

# NNIE_tutorial
根据自身项目经验,结合华为的官方文档和样例写的教程,目前第三Part完整的SSD模型样例已经更新完,yolo的部分会逐步更新.

### 注意

2020-12-21:感谢来自华为得认可(https://github.com/liuky74/SDC-NNIE-tutorial/issues/1) ,如果各位拿到的demo已经是C++版本的了,那么本项目仅能作为参考

2020-09-01:原本dev分支为主分支,现已将dev分支改为测试版本分支,在功能完成后会合并到master下
### 前期准备
- 你需要一台华为的SDC摄像机用于调试,或者使用华为的一站式开发平台(http://113.200.78.43:8088/)
- 只有代码也是不行的,你还需要一份华为的开发文档,这个需要向华为的客服索要
- 最后,使用本项目的代码是建立在已经成功的将caffe模型转换为NNIE的wk模型以后,关于caffe的知识暂且不涉及

### 主要内容
- 由浅入深的对SDC(Software Defined Camera 软件定义相机)进行讲解,项目中的代码中有大量的中文注释,配合注释基本可以快速弄懂SDC以及NNIE框架的使用方法.
- 教程的最后将封装好的API以:
   - 加载模型
   - 获取图像
   - 模型推导
   - 获得结果
   
   这4步来进行一个完整的SSD模型加载样例,帮助读者快速进行工业部署.
## 注意
#### 教程是循序渐进的,因此后部分的代码都会包含前部分的代码(比如Part3会包含Part2的代码,并且往往代码结构会更加规范),因此如果是工程使用那么直接用最新一Part的代码即可

项目结构:
- Part_1: 该文件夹下的为video.iaas.sdc服务的教程样例,摄像头视频数据IO相关
- Part_2 该文件夹下为algorithem.iaas.sdc服务的教程样例,包含图像转换以及模型加载等相关操作
  - 图像转换(已更新)
  - 模型加载(已更新)
- Part_3 该文件夹为algorithem.iaas.sdc服务的教程样例,包含模型加载,SSD模型的初始化以及后处理函数,前向推导等操作
  - 模型初始化(已更新)
  - 后处理函数(已更新)
  - 前向推导函数(已更新)
  - 检测结果的处理与显示(已更新)
### 主要贡献
- 迁移到C++平台上,现在各大服务都集成为类的形式进行调用了
- 添加了CMAKE用的文件,现在使用CLION等IDE能够很好的进行代码补全,加快写代码的速度
- 对华为海思SDC的API进行了封装,原先华为给的demo非常乱,现在各类服务的注册和通讯都封装在了各个类方法中,对用户透明化
- 修正了样例代码的一些小BUG


