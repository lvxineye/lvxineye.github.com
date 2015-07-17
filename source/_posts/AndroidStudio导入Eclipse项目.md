title: "AndroidStudio导入Eclipse项目"
date: 2015-07-03 11:28:39
categories:
tags:
---
AndroidStudio 导入Eclipse项目两种方法：兼容Eclipse和Android Gradle Project。
转载自:[http://www.cnblogs.com/ct2011/p/4183553.html](http://www.cnblogs.com/ct2011/p/4183553.html)


## 兼容模式
这种模式下，保证了Eclipse时代的代码目录结构，整体操作和使用和Eclipse也差不多。
最重要的，当你使用AndroidStudio时，你或者其他人也可以方便的使用Eclipse，互不干扰。
同时也不用改变svn/git的上的代码库结构

### 步骤

#### 1. 从Eclipse中导出Gradle build files

- 在Eclipse菜单中 File --> Export-->Generate Gradle build files

![image](/img/studio_eclipse_1.png)

- 接下来会到达警告界面，这里会提示AndroidStudio可以直接导入ADT的工程，先过，后面有直接导入的讲解。

![image](/img/studio_eclipse_2.png)

- 选中你的项目工程，包括主工程和库工程（Library）。

![image](/img/studio_eclipse_3.png)

- 确认生成

![image](/img/studio_eclipse_4.png)

#### 2. 修改导出文件参数
导出后，由于adt很久没更新，需要手动改一些参数，才能保证正常使用。

**没有库工程，只有主工程**
这种情况下你看到的目录是这样的

![image](/img/studio_eclipse_5.png)

- 首先需要更改的是 build.gradle 文件

![image](/img/studio_eclipse_6.png)

- 然后还需要更新Gradle版本，指定为所需要的2.2.1

![image](/img/studio_eclipse_7.png)

**含有库工程**
其实改动方法和上面一样，只需要注意是改动整个项目的build.gradle和 /gradle/wrapper/gradle-wrapper.properties。
而不要尝试去主工程或者库工程里面找build.gradle

![image](/img/studio_eclipse_8.png)

#### 3. 导入AndroidStudio
- 进入到AndroidStudio中，选择导入非AndroidStudio工程

![image](/img/studio_eclipse_9.png)

- 找到需要导入的工程目录，可以看到图标和Eclipse创建的工程不一样。

![image](/img/studio_eclipse_10.png)

- 点击OK，进入漫长的加载过程，之后就可以正常使用了。

![image](/img/studio_eclipse_11.png)
