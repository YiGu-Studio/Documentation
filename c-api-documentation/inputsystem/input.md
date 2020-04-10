# Input

这个静态类提供输入功能，基本的输入系统不需要要绑定任何事件（events）与支持。输入系统的用法很大程度上是不言自明的，但是也有少许容易误用的构造。

## 按键获取

`GetKeyDown(KeyCode)` \| `GetKeyPressed(KeyCode)` \| `GetKeyReleased(KeyCode)` -是最常用的方法。当按键被按下时，`GetKeyDown`将会持续每一帧都返回true，这可能导致不够理想的运行情况。如果你一次只想读一次输入数据，使用`GetKeyPressed` 或者 `GetKeyReleased`。

你也可以使用`IsDown`/`IsPressed`/`IsReleased`这种扩展方法，比如`KeyCode.A.IsPressed()`。

