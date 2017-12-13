# VideoConversionTool
基于FFmpeg的视频转换小公举，啊不是，是小工具

## 1. 视频格式
默认格式是 wmv->mp4

如需修改，请右键打开编辑，修改SourceFileType为你的待转换视频格式，修改TargetFileType为你的目标视频格式。切记“=”符号两边不能有空格！不能有空格！不能有空格！

支持的视频格式，请参考FFmpeg官方支持格式。

## 2. 使用方式

### 2.1 安装FFmpeg

需安装FFmpeg。请移步：[https://www.ffmpeg.org/download.html](https://www.ffmpeg.org/download.html)

### 2.2 运行本脚本

本脚本为Shell脚本，将本脚本放在需要转换的目录的**根目录**即可。可直接运行如下

```shell
$ ./VideoConversionTool
```

如无权限，则需chmod。你懂得

### 2.3 视频流向

脚本默认读取源视频所在文件目录，转换完的视频同样存储在源视频目录内。

## 3. 免责声明

本脚本为闲暇之余开发娱乐之用。如需商用，请认真审查代码，并适当做出修改。本人不承担任何法律责任。

本脚本在macOS High Sierra下测试通过。

## 4. 更新日志

### 2017.12.13

- 新增日志监控，随时随地了解转码过程的最新动态
- 规避转码失败的视频，保留转码失败的原始视频
- 新增视频使用ffmpeg自带的aac音频解码。如仍不能按照严格模式解码音频，请右键编辑脚本，然后自行去掉`-strict -2`字符