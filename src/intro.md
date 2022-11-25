# KiviBot 简介 {#KiviBot}

一个使用 `TypeScript` 语言编写，**轻量**、**跨平台**的 QQ 机器人框架。

核心 QQ 协议基于 [oicq][1]，项目初衷在于提高群活跃氛围、方便群管理，仅供个人娱乐、学习交流使用，**不得将本项目用于任何非法用途**。

## 框架特征

- ⚡ **轻量、高效**: 无需运行 UI 界面，内存占用低。 开发语言与底层协议一致，执行效率高，框架依赖少。（10~20 MB）

- 📱 **跨平台**: Windows，Linux，手机和平板都能运行。（移动设备需安装终端模拟器，如 Termux，iSH）

- 📦 **优雅、便携**: 支持手机、平板、手表和 MacOS 协议。 使用 QQ 消息控制机器人，无需远程连接服务器进行操作。

- 💻 **开发者友好**: 学习门槛低，只需几行 JS/TS 代码就能编写插件，支持热重载，拥有完备的脚手架与 TS 类型定义。

更多特征等你探索...

## 插件示例

仅需编写少量 `JavaScript` 代码即可实现非常简单的 Hello World 插件。

```js
const { KiviPlugin } = require('@kivibot/core')

const plugin = new KiviPlugin('JS 插件模板', '0.1.0')

plugin.onMounted((bot, admins) => {
  plugin.onCmd('Hello', (e, args) => e.reply('World')) // [!code hl]
})

module.exports = plugin
```

可见，只要你有 `JavaScript` 语言的基础，上手开发一个插件是非常简单的。

[1]: https://github.com/takayama-lily/oicq
[2]: https://github.com/takayama-lily/abot
[3]: https://www.npmjs.com/package/pm2
