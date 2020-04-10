# Scene

Scenes(场景)是指当前游戏中已加载的实例化视图。

## 提示

* 你可以通过 `Mission.Current.Scene`去获取当前场景，前提是`Mission.Current`是非空引用，并且场景已经被加载。

* 你可以通过`/Modules/_MODULENAME_（模块名）/SceneObj/`这个文件目录去获取场景的静态信息.

### 查找场景的示例

**注意**: 你**不应该**直接修改默认的游戏文件。

每个模块的场景文件位于相对应模块的`SceneObj`文件夹。例如，SandBoxs(沙盒)场景文件的目录位于`/Modules/SandBox/SceneObj`。

在本例中，该场景的路径是: `/Modules/SandBox/SceneObj/arena_aserai_a`。 使用首选文本编辑器打开`scene.xscene`。

在该场景文件的第二行，包含了这个特殊场景的名字。

`<scene name="arena_aserai_a" version="2">` 从这里得知，场景的名字是`arena_aserai_a`。

然后根据这个名字，在代码里面检查当前的场景是否与这个名字相同。

```csharp
if(Mission.Current.SceneName == "arena_aserai_a")
{
    // ...
}
```

