# ffmpeg_go
## 请自行安装ffmpeg。安装好后，将bin目录配置到环境变量中即可。
#### 请将main.go与需要处理的视频文件放在同一文件夹下（支持多个子文件夹），未打包情况下使用 go run 命令执行。windows环境下打包直接双击生成的exe文件。填写对应生成截图的宽度与高度。程序将自动生成视频时长1/3处的截图。保存在与视频同级目录下。

### 通过go build生成的exe文件,通常是一个默认的图标,发给别人的时候,总觉得像病毒,下面我们来给他加一个好看的图标,让他看起来正经一些.
#### 1.找到一个喜欢的图片.
#### 2.通过工具或是在线工具生成.ico的图标文件(假定是main.ico)
#### 3.进入到项目的目录(执行go build的地方)
#### 4.创建一个空白文本文件,命名main.rc
#### 5.记录本打开,输入并保存 IDI_ICON1 ICON "main.ico" 
#### 6.在项目目录执行下面的命令 windres -o main.syso main.rc ,此时生成了一个main.syso
#### 7.直接go build, 生成的exe就有了一个好看的图标了.
