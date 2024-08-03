# 环境配置问题

## YOLOv5-NPU

### 配置地址：

https://gitee.com/ascend/modelzoo-GPL/tree/master/built-in/PyTorch/Official/cv/object_detection/Yolov5_for_PyTorch_v6.0

https://www.hiascend.com/document/detail/zh/ModelZoo/pytorchframework/ptes/ptes_00001.html

### 配置环境：

#### ARM架构下的虚拟容器，用conda构建

## ![npu训练环境搭建流程](D:\c++\找工作\实习\潍柴动力\图\npu训练环境搭建流程.png)

## 1.YOLOv5-NPU版本要求

### python    3.9

### gcc              >9.0

## 2.过早的文件结束符（EOF）

![dbc9eceea371aacf820678361c50410](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\dbc9eceea371aacf820678361c50410.jpg)

### 解决方法：文件太大，需要扩大 传输限制

```bash
git config --global http.postBuffer 524288000
git config --list
执行上述命令后看到如下结果
http.postbuffer=524288000
```

## 3.error：invalid command 'bdist_wheel'

### apt install wheel

## 4.E:Unable to locate package wheel

### 镜像内报错，解决方法更新apt update

## 5.invalid index-pack output

![4378edcabf09f6b194bcf55b3b3ce74](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\4378edcabf09f6b194bcf55b3b3ce74.jpg)

### 解决方法：文件太大，需要扩大 传输限制

```bash
git config --global http.postBuffer 524288000
git config --list
执行上述命令后看到如下结果
http.postbuffer=524288000
```

## 6.msnpureport command not found

![52302de459e66faca30266b08a6110a](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\52302de459e66faca30266b08a6110a.jpg)

### 原因：msnpureport工具不支持容器场景，部署容器时，禁止将msnpureport工具映射到容器内

![19161b978cce2628692434825118496](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\19161b978cce2628692434825118496.jpg)

### 解决方法：msnpureport具有导出日志功能，注释掉msnpureport有关的代码

## 7.awk报错：语法错误

![d3b66956ec9d3d75449aebfb7e3ecf9](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\d3b66956ec9d3d75449aebfb7e3ecf9.jpg)

### 1.原因分析：查看文件train_yolov5s_performance_1p.sh,发现如下apt 图一段代码可能存在问题，查找train_${ASCEMD_DEVICE_ID}.log日志文件

![fbeaee4d98b397d85f8631203bd0584](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\fbeaee4d98b397d85f8631203bd0584.jpg)

### 2.发现日志报错如下：no module named 'torch_npu'

![70b9a46ecf891ff393ef6098be2c10c](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\70b9a46ecf891ff393ef6098be2c10c.jpg)

### 3.查找服务器CANN版本地址，/usr/local/Ascend/version.info,如下所示：

![06457460bce72a2e139e1d306c24c90](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\06457460bce72a2e139e1d306c24c90.jpg)

### 4.更新torch-npu版本

## 8.no module named 'apex'

### 安装apex，pip install apex报错：

![79dce070d29297ff1004d3fc38b78db](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\79dce070d29297ff1004d3fc38b78db.jpg)

### 官网安装：https://www.hiascend.com/document/detail/zh/ModelZoo/pytorchframework/ptes/ptes_00001.html

## 9.报错RPC failed；curl 92 HTTP/2 stream 0 was not closed  cleanly:CANCEL(err 8)

![4cacb1756861dac94c87a8c4a918fbf](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\4cacb1756861dac94c87a8c4a918fbf.jpg)

### 解决方法：清空缓存git clean -f，或者等待网络变好

## 10.报错：could not find。。。（QNNPACK）

![3cc1bca5aad4f0b6f5a1b24fa0a8864](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\3cc1bca5aad4f0b6f5a1b24fa0a8864.jpg)

### 解决方法:删除QNNPACK，重新git submodule update --init --recursive![3cc1bca5aad4f0b6f5a1b24fa0a8864](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\3cc1bca5aad4f0b6f5a1b24fa0a8864.jpg)

## 11.报错：failed to compile the wheel

![afb46f71bc617c09320a68305549599](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\afb46f71bc617c09320a68305549599.jpg)

### 重新编译一遍错误消失

## 12.报错：libpython3.9.so：can not open shared object file:no such file or directory

![d3dd371aad92f41a7a39c15496003bf](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\d3dd371aad92f41a7a39c15496003bf.jpg)

### 通过find查找，发现环境中存在该共享文件：

![397f5a1ad49c8f3252a080c85ce195c](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\397f5a1ad49c8f3252a080c85ce195c.jpg)

### 最后发现pytorch版本过老，重新安装

## 13.缺少一系列包如图所示

![2cb7ec4f3648d3151699243ed065730](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\2cb7ec4f3648d3151699243ed065730.jpg)

![f17ef017c8c5947ea4c81d9de8c6174](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\f17ef017c8c5947ea4c81d9de8c6174.jpg)

### 依次安装即可

## 14.valueError，but not set

![22677939df89ef85893ab32a161f487](C:\Users\wangyichen\Documents\WeChat Files\wxid_h08rd7gkgblg22\FileStorage\Temp\22677939df89ef85893ab32a161f487.jpg)

### 设置主机服务器和端口号

### 采用单机多卡训练

## 15.报错：unexpected bus error encountered in worker

![0cc43f2077c90d94ccffa26d6c2646d](C:/Users/wangyichen/Documents/WeChat%20Files/wxid_h08rd7gkgblg22/FileStorage/Temp/0cc43f2077c90d94ccffa26d6c2646d.jpg)

### 将worker参数从32降为8以下，我降为0
