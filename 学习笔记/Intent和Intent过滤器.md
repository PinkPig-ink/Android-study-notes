# Intent 和 Intent 过滤器

`Intent` 是一个消息传递对象，您可以用来从其他[应用组件](https://developer.android.com/guide/components/fundamentals#Components)请求操作。

尽管 Intent 可以通过多种方式促进组件之间的通信，但其基本用例主要包括以下三个：

- **启动Activity**

  `Activity` 表示应用中的一个屏幕。

  通过将 `Intent` 传递给 `startActivity()`，您可以启动新的 `Activity` 实例。

  `Intent` 用于描述要启动的 Activity，并携带任何必要的数据。

- **启动服务**

  `Service` 是一个不使用用户界面而在后台执行操作的组件。

- **传递广播**

  广播是任何应用均可接收的消息。

## Intent 类型

Intent 分为两种类型：

- **显示 Intent**

  通过提供目标应用的软件包名称或完全限定的组件类名来指定可处理 Intent 的应用。

  当 `Intent` 对象显式命名某个具体的 Activity 组件时，系统立即启动该组件。

  

- **隐式 Intent**

  不会指定特定的组件，而是声明要执行的常规操作，从而允许其他应用中的组件来处理。

  ![img](https://developer.android.com/images/components/intent-filters_2x.png)