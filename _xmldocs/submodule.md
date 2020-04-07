# SubModule \(XML\)

## 字段介绍

* `Name` - 模组的名字
* `Id` - 模组的ID\(不允许空格\)
* `Version` - 模组版本
* `SinglePlayerModule` - 是否单机模组
* `MultiPlayerModule` - 是否联机模组
* `DependedModules` - 依赖的模组
* `SubModules` - 模组包含的子模块\(DLLs\)
* `Xmls` - ModuleData文件夹中的XML文件路径.

## 重点

不同模组中的同ID的XML文件中的内容会被组合而**不会覆盖**，这些文件中相同ID的东西会根据读取顺序覆盖之前加载的内容。

`MPClassDivisions` 目前不可用

## 例子

```xml
<Module>
    <Name value="My Module"/>
    <Id value="MyModule"/>
    <Version value="v1.0.0"/>
    <SingleplayerModule value="true"/>
    <MultiplayerModule value="false"/>
    <DependedModules>
        <DependedModule Id="Native"/>
        <DependedModule Id="SandBoxCore"/>
        <DependedModule Id="Sandbox"/>
        <DependedModule Id="CustomBattle"/>
        <DependedModule Id="StoryMode" />
    </DependedModules>
    <SubModules>
        <!-- 子节点是可选的，如果没有DLL的话就不需要这部分。 -->
        <SubModule>
            <Name value="MySubModule"/>
            <!-- DLL文件路径  -->
            <DLLName value="ExampleMod.dll"/>
            <SubModuleClassType value="ExampleMod.MySubModule"/>
            <Tags>
                <Tag key="DedicatedServerType" value="none" />
                <Tag key="IsNoRenderModeElement" value="false" />
            </Tags>
        </SubModule>
    </SubModules>
    <Xmls>
        <XmlNode>
            <XmlName type="1" id="Items" path="customitems"/>
        </XmlNode>  
        <XmlNode>
            <XmlName type="1" id="SPCultures" path="customcultures"/>
        </XmlNode>
        <XmlNode>
            <XmlName type="1" id="NPCCharacters" path="customcharacters"/>
        </XmlNode>
    </Xmls>
</Module>
```

