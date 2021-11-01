# face_recognition - windows 安装

> 1V



#### 1. 安装cmake

```
https://cmake.org/download/
```

#### 2. 安装VS依赖库 / 或者VS（选择C++编译包）

```
https://aka.ms/vs/16/release/vc_redist.x64.exe
```

#### 3. 安装dlib

从[https://pypi.org/simple/dlib/]()下载tar.gz包，解压后进入目录执行

```
python setup.py install --no DLIB_GIF_SUPPORT
```

将build/lib.win-amd64-**的pyd文件放到python安装目录的DLLs下

#### 4.  安装face_recognition

```
pip install face_recognition
```

