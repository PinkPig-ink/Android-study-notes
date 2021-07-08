# 消息框概览

消息框可以在一个小型弹出式窗口中提供与操作有关的简单反馈。它只会填充消息所需的空间大小，并且当前 Activity 会一直显示及供用户与之互动。

超时后，消息框会自动消失。

## 消息框的替代方案

- 前台运行

  考虑使用[信息提示控件](https://material.io/components/snackbars)代替消息框，信息提示控件中包含用户可操作的选项，可提供更好的应用体验。

- 后台运行

  如果您的应用在后台运行，并且您希望用户执行某项操作，请改用[通知](https://developer.android.com/guide/topics/ui/notifiers/notifications)。

### 示例化Toast对象

使用 `makeText()`，该方法采用以下参数：

1. 应用 `Context`
2. 应向用户显示的文本
3. 消息框停留时长

`makeText()`方法会返回正确初始化的`Toast`对象

### 显示消息框

使用Toast对象的 show 方法

```java
Context context = getApplicationContext();
CharSequence text = "Hello toast!";
int duration = Toast.LENGTH_SHORT;

Toast toast = Toast.makeText(context, text, duration);
toast.show();
```

### 链式调用消息框方法

```Java
Toast.makeText(context, text, duration).show();
```

