# VoiceReplyFree
**大家帮忙点点star 谢谢啦!**

VoiceReplyFree是一个基于[VoiceReply](https://github.com/flyhunterl/VoiceReply)的分支项目，它使用[Pollinations.ai](https://pollinations.ai/)的语音服务来生成语音回复，无需配置TTS模型。使用前需参照[VoiceReply](https://github.com/flyhunterl/VoiceReply)中的语音信息配置部分进行配置

## 功能特点

* 支持文本到语音的转换
* 使用配置的大语言模型生成回答
* 使用Pollinations.ai的语音合成服务生成自然的语音
* 支持自定义语音模型和声音
* 内置错误处理和重试机制
* 兼容DOW插件扫描机制

## 使用方法

1. 发送格式：  
   * `语音+您的问题`  
   * `语音 您的问题`  
   * `语音您的问题`
2. 示例：  
   * `语音+今天天气怎么样`  
   * `语音 介绍一下你自己`  
   * `语音讲个笑话`

## 安装方法

1. 将整个 `VoiceReplyFree` 文件夹复制到DOW框架的 `plugins` 目录下（注意文件夹名称必须与插件名称一致）
2. 确保已安装所需依赖：`pip install requests`
3. 重启DOW应用程序

## 配置说明

在`config.json`文件中可以配置以下参数：

```json
{
    "chat": {
        "base": "API基础URL",
        "api_key": "API密钥",
        "model": "聊天模型名称",
        "temperature": 温度值
    },
    "pollinations": {
        "base": "Pollinations API基础URL",
        "model": "语音模型",
        "voice": "语音音色"
    }
}
```

可用的Pollinations语音音色包括：alloy, echo, fable, onyx, nova, shimmer, ballad等。

## 注意事项

1. 使用前请确保已正确配置Chat API密钥
2. 语音生成可能需要一定时间，请耐心等待
3. 如果语音生成失败，插件会自动返回文字回答
4. 本插件已按DOW标准格式重构，能够被DOW框架正确识别

## 错误处理

1. API请求失败时会自动重试3次
2. 生成的语音文件为空时会自动清理并返回错误信息
3. 配置文件加载失败时会使用默认配置

## 鸣谢
- [dify-on-wechat](https://github.com/hanfangyuan4396/dify-on-wechat) - 本项目的基础框架
- [SearchMusic](https://github.com/Lingyuzhou111/SearchMusic) - 项目思路来源
- [Gewechat](https://github.com/Devo919/Gewechat) - 微信机器人框架，个人微信二次开发的免费开源框架 


## 打赏

如果您觉得这个项目对您有帮助，欢迎打赏支持作者继续维护和开发更多功能！

![20250314_125818_133_copy](https://github.com/user-attachments/assets/33df0129-c322-4b14-8c41-9dc78618e220)
