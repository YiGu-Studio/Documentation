# Input

`Input`这个静态类型提供输入功能。霸主中，基本的输入系统并不是基于事件绑定的，而是采用轮询的方式。关于输入的调用，绝大部分很直观，从函数名就能明白什么意思，但也会有几个坑。

## Key Polling

`GetKeyDown(KeyCode)` | `GetKeyPressed(KeyCode)` | `GetKeyReleased(KeyCode)` - 这几个貌似是最常用的方法了。 关于 `GetKeyDown` 请注意：只要键盘按键处于按下状态，程序就会在每一帧持续不断地返回`true`，显然这会导致运行一些不必要的方法\(造成资源浪费\)。假如你纯粹只想让按键触发一次操作，可以用`GetKeyPressed` 或者 `GetKeyReleased`。

还有几个扩展方法也可以达到同样效果  `IsDown`/`IsPressed`/`IsReleased` 比如 `KeyCode.A.IsPressed()`。