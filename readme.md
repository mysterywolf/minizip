# Minizip for RT-Thread

[Minizip](http://www.winimage.com/zLibDll/minizip.html) 是依托于[zlib软件包](https://github.com/RT-Thread-packages/zlib)的一个zip格式解、压缩的软件包。



## 主要接口文件

- zip.c：负责将多文件压缩为zip压缩包相关
- unzip.c：负责zip压缩包解压相关 



## 提供解压缩命令2个

### 1. miniunz 命令

负责解压zip压缩包，命令如下：

```shell
Usage : miniunz [-e] [-x] [-v] [-l] [-o] [-p password] file.zip [file_to_extr.] [-d extractdir]

  -e  Extract without pathname (junk paths)
  -x  Extract with pathname
  -v  list files
  -l  list files
  -d  directory to extract into
  -o  overwrite files without prompting
  -p  extract crypted file using password
```

一般，用`-e`命令来解压提取，用`-l`或`-v`命令来列出压缩包内的文件。

### 2. minizip命令

负责将多文件压缩为zip压缩包，命令如下：

```shell
Usage : minizip [-o] [-a] [-0 to -9] [-p password] file.zip [files_to_add]

  -o  Overwrite existing file.zip
  -a  Append to existing file.zip
  -0  Store only
  -1  Compress faster
  -9  Compress better
```



## 如何获取软件包

可通过 env 工具辅助下载：

```
RT-Thread online package -> 
     miscellaneous package -> 
         [*] minizip: zip manipulation library --->
```



## 注意

如果只是列出zip压缩包的文件，该操作不会占用多少内存。但是如果要进行解、压缩操作，需要占用很大的内存，至少100KB左右，建议使用配备外置SRAM的开发板进行尝试。



## 维护

[Meco Man](https://github.com/mysterywolf) @ RT-Thread Community

https://github.com/mysterywolf/minizip



