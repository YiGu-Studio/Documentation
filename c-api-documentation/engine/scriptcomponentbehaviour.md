# ScriptComponentBehaviour


从风车旋转的动画，到创建自定义的武器生成器，或者全新的攻城武器——ScriptComponentBehaviour可以用来做很多事情。

一个`TaleWorlds.MountAndBlade.dll`的`LumberJack`类中，关于ScriptComponentBehaviour的基础例子：

```csharp
    public class Lumberjack : ScriptComponentBehaviour
    {
        private bool _initialized;

        protected internal override void OnTick(float dt)
        {
            base.OnTick(dt);
            if (!this._initialized)
            {
                this._initialized = true;
                base.GameEntity.CreateSimpleSkeleton("human_skeleton");
                base.GameEntity.CopyComponentsToSkeleton();
                base.GameEntity.Skeleton.SetAnimationAtChannel("lumberjack", 0, 1f, -1f, 0f);
                MetaMesh copy = MetaMesh.GetCopy("peasent_hatchet", true, false);
                base.GameEntity.AddMultiMeshToSkeletonBone(copy, 27);
            }
        }
    }
```



\*\* 注意: 这里最好重写`OnInit()`而不是使用 `OnTick()`。因为按照TaleWorlds的写法，这个例子的代码将随着时间一直运行。

可能的原因：网格不能在OnInit中被编辑/生成，你可能得等一个Tick，否则游戏会崩溃。

