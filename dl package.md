我在windows下把包安好了，不过我没有用anaconda，就纯自己一个一个装。

我就按照教程里说的这个走的：  
pip 安装 geopandas之前，要先从 http://www.lfd.uci.edu/~gohlke/pythonlibs 下载  
Fiona , GDAl , pyproj , Shapely，分别进行安装，否则可能会报错。

其中Fiona又是依赖于GDAl的，所以得先安GDAl。  
不过GDAl和pyproj本身又是需要 `visual c++ 14.0`

当然你可以先试着安装GDAl，如果提示你没有 c++14的话，你可以从这个地址下  
http://go.microsoft.com/fwlink/?LinkId=691126&fixForIE=.exe.

然后还有一点，这几个python好像不能直接用pip install下，会报一个我也看不太懂的错误，只能是像上面说的那样，在那个网站上先下载whl文件（例如下载的是 xxx.whl），然后再运行 `pip install xxx.whl`

不过每个whl文件有很多版本，`一定要下对版本，否则用不了`  
例如对于 `GDAl`，有  
GDAL‑1.11.4‑cp27‑none‑win_amd64.whl  
GDAL‑2.1.4‑cp27‑cp27m‑win32.whl  
GDAL‑2.1.4‑cp27‑cp27m‑win_amd64.whl  
GDAL‑2.1.4‑cp34‑cp34m‑win32.whl  
GDAL‑2.1.4‑cp34‑cp34m‑win_amd64.whl  
GDAL‑2.1.4‑cp35‑cp35m‑win32.whl  
GDAL‑2.1.4‑cp35‑cp35m‑win_amd64.whl  
GDAL‑2.1.4‑cp36‑cp36m‑win32.whl  
GDAL‑2.1.4‑cp36‑cp36m‑win_amd64.whl  
GDAL‑2.2.4‑cp27‑cp27m‑win32.whl  
GDAL‑2.2.4‑cp27‑cp27m‑win_amd64.whl  
GDAL‑2.2.4‑cp34‑cp34m‑win32.whl  
GDAL‑2.2.4‑cp34‑cp34m‑win_amd64.whl  
GDAL‑2.3.2‑cp35‑cp35m‑win32.whl  
GDAL‑2.3.2‑cp35‑cp35m‑win_amd64.whl  
GDAL‑2.3.2‑cp36‑cp36m‑win32.whl  
GDAL‑2.3.2‑cp36‑cp36m‑win_amd64.whl  
`GDAL‑2.3.2‑cp37‑cp37m‑win32.whl`  
`GDAL‑2.3.2‑cp37‑cp37m‑win_amd64.whl`  

举个例子，cp37代表是python3.7，win32指支持32位windows系统，balabala，就下和你本机环境对应的包即可。

你如果不知道本机是什么的话，那就一个一个试，假如python版本是3.7，你就把标红的两个都下下来看哪个能安就完事了。其余以此类推。

四个都装好之后再安装geopandas，可以直接用pip装。

最后，我发现我给你发的那个链接里的代码直接用不了，我也不知道为什么，所以你还是用你最初的那个吧。
