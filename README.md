免费又好用的语音识别引擎----Vosk

vosk是一个离线开源语音识别工具，它可以识别16种语言，包括中文，而且总体效果还是不错的，因为我们要对接到呼叫中心，因此我们需要实时的流式传输语音数据，目前主流的解决方案是采用websocket协议传输语音，这块的话Vosk直接提供了websocket的server程序。而且程序已经打包成docker发布，所以启动起来相当简单，真的很贴心，一句命令搞定：

docker run -d -p 2700:2700 alphacep/kaldi-cn:latest


mod_vosk 编译Makefile需要处理一下，编辑在fs的src/mod下目录编译即可
