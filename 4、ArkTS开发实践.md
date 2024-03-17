# ArkTS开发实践

## 声明式UI基本概念

应用界面是由一个个页面组成，ArkTS是由ArkUI框架提供，用于以声明式开发范式开发界面的语言。

声明式UI构建页面的过程，其实是组合组件的过程，声明式UI的思想，主要体现在两个方面：

- 描述UI的呈现结果，而不关心过程
- 状态驱动视图更新

类似苹果的SwiftUI中通过组合视图View，安卓Jetpack Compose中通过组合@Composable函数，ArkUI作为HarmonyOS应用开发的UI开发框架，其使用ArkTS语言构建自定义组件，通过组合自定义组件完成页面的构建。

## 自定义组件的组成

ArkTS通过struct声明组件名，并通过@Component和@Entry装饰器，来构成一个自定义组件。

使用@Entry和@Component装饰的自定义组件作为页面的入口，会在页面加载时首先进行渲染。

```
@Entry@Componentstruct ToDoList {...}
```

例如ToDoList组件对应如下整个代办页面。

**图1** ToDoList待办列表
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.91214364955715909264777485658456:50001231000000:2800:BF8C61AD8B160CBCE842CFC9BA823EDA1F3346AF2F04B5BC98D12EC25594F627.png?needInitFileName=true?needInitFileName=true)

使用@Component装饰的自定义组件，如ToDoItem这个自定义组件则对应如下内容，作为页面的组成部分。

```
@Componentstruct ToDoItem {...}
```



**图2** ToDoItem
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.70864399038839262983204054952903:50001231000000:2800:82907EBD1EA58D368839B0174A0A57CAC9069CF2C746C9FCE5605DF679E8D992.png?needInitFileName=true?needInitFileName=true)



在自定义组件内需要使用build方法来进行UI描述。

```
@Entry@Component struct ToDoList   ...   build() {    ...  } }
```



build方法内可以容纳内置组件和其他自定义组件，如Column和Text都是内置组件，由ArkUI框架提供，ToDoItem为自定义组件，需要开发者使用ArkTS自行声明。

```
@Entry@Componentstruct ToDoList {  ...  build() {    Column(...) {      Text(...)        ...      ForEach(...{        TodoItem(...)      },...)    }  ...  }}
```

## 配置属性与布局

自定义组件的组成使用基础组件和容器组件等内置组件进行组合。但有时内置组件的样式并不能满足我们的需求，ArkTS提供了属性方法用于描述界面的样式。属性方法支持以下使用方式：

- 常量传递

  例如使用fontSize(50)来配置字体大小。

  ```
  Text('Hello World')  .fontSize(50)
  ```

- 变量传递

  在组件内定义了相应的变量后，例如组件内部成员变量size，就可以使用this.size方式使用该变量。

  ```
  Text('Hello World')  .fontSize(this.size)
  ```

- 链式调用

  在配置多个属性时，ArkTS提供了链式调用的方式，通过'.'方式连续配置。

  ```
  Text('Hello World')  .fontSize(this.size)  .width(100)  .height(100)
  ```

- 表达式传递

  属性中还可以传入普通表达式以及三目运算表达式。

  ```
  Text('Hello World')  .fontSize(this.size)  .width(this.count + 100)  .height(this.count % 2 === 0 ? 100 : 200)
  ```

- 内置枚举类型

  除此之外，ArkTS中还提供了内置枚举类型，如Color，FontWeight等，例如设置fontColor改变字体颜色为红色，并私有fontWeight为加粗。

  ```
  Text('Hello World')  .fontSize(this.size)  .width(this.count + 100)  .height(this.count % 2 === 0 ? 100 : 200)  .fontColor(Color.Red)  .fontWeight(FontWeight.Bold)
  ```

对于有多种组件需要进行组合时，容器组件则是描述了这些组件应该如何排列的结果。

ArkUI中的布局容器有很多种，在不同的适用场合选择不同的布局容器实现，ArkTS使用容器组件采用花括号语法，内部放置UI描述。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.07898287615434915086334324058918:50001231000000:2800:AED8D775381759D514C971F010077187141B17BEDFE8AC7C006F1E9808CEEAF1.png?needInitFileName=true?needInitFileName=true)

这里我们将介绍最基础的两个布局——列布局和行布局。

对于如下每一项的布局，两个元素为横向排列，选择Row布局

**图3** Row布局
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.93120900297637334462488161323853:50001231000000:2800:1AA8CA6A161F92DD29180F12AEE850BAC8C52E1EE4ECC4C30FEF159D48F7DA47.png?needInitFileName=true?needInitFileName=true)

```
Row() {  Image($r('app.media.ic_default'))    ...  Text(this.content)     ...}...
```

类似下图所示的布局，整体都是从上往下纵向排列，适用的布局方式是Column列布局。

**图4** Column布局
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.63385695838810553969799111570592:50001231000000:2800:7BE4043F45BF4887705D6A40708EFD17FEAC0A0DFD18C2B2587D60B2EB2B9E04.png?needInitFileName=true?needInitFileName=true)

```
Column() {   Text($r('app.string.page_title'))     ...
   ForEach(this.totalTasks,(item) => {     TodoItem({content:item})   },...) }
```

## 改变组件状态

实际开发中由于交互，页面的内容可能需要产生变化，以每一个ToDoItem为例，其在完成时的状态与未完成时的展示效果是不一样的。

**图5** 不同状态的视图
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.93238860542154486009397481868482:50001231000000:2800:8247D52C6DA28400C896FB027EED0986AA63A128FD8BA55F45F62F416CE6EC58.png?needInitFileName=true?needInitFileName=true)

声明式UI的特点就是UI是随数据更改而自动刷新的，我们这里定义了一个类型为boolean的变量isComplete，其被@State装饰后，框架内建立了数据和视图之间的绑定，其值的改变影响UI的显示。

```
@State isComplete : boolean = false;
```

**图6** @State装饰器的作用
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.31593490334415164900685410896927:50001231000000:2800:BAF1561160F70AF221ED23AD7E3E5DD85DED36C72B5AD9D2CB0370BC044453BE.png?needInitFileName=true?needInitFileName=true)



用圆圈和对勾这样两个图片，分别来表示该项是否完成，这部分涉及到内容的切换，需要使用条件渲染if / else语法来进行组件的显示与消失，当判断条件为真时，组件为已完成的状态，反之则为未完成。

```
if (this.isComplete) {  Image($r('app.media.ic_ok'))    .objectFit(ImageFit.Contain)    .width($r('app.float.checkbox_width'))    .height($r('app.float.checkbox_width'))    .margin($r('app.float.checkbox_margin'))} else {  Image($r('app.media.ic_default'))    .objectFit(ImageFit.Contain)    .width($r('app.float.checkbox_width'))    .height($r('app.float.checkbox_width'))    .margin($r('app.float.checkbox_margin'))}
```

由于两个Image的实现具有大量重复代码，ArkTS提供了@Builder装饰器，来修饰一个函数，快速生成布局内容，从而可以避免重复的UI描述内容。这里使用@Bulider声明了一个labelIcon的函数，参数为url，对应要传给Image的图片路径。

```
@Builder labelIcon(url) {  Image(url)    .objectFit(ImageFit.Contain)    .width($r('app.float.checkbox_width'))    .height($r('app.float.checkbox_width'))    .margin($r('app.float.checkbox_margin'))}
```

使用时只需要使用this关键字访问@Builder装饰的函数名，即可快速创建布局。

```
if (this.isComplete) {  this.labelIcon($r('app.media.ic_ok'))} else {  this.labelIcon($r('app.media.ic_default'))}
```

为了让待办项带给用户的体验更符合已完成的效果，给内容的字体也增加了相应的样式变化，这里使用了三目运算符来根据状态变化修改其透明度和文字样式，如opacity是控制透明度，decoration是文字是否有划线。通过isComplete的值来控制其变化。

```
Text(this.content)  ...  .opacity(this.isComplete ? CommonConstants.OPACITY_COMPLETED : CommonConstants.OPACITY_DEFAULT)  .decoration({ type: this.isComplete ? TextDecorationType.LineThrough : TextDecorationType.None })
```

最后，为了实现与用户交互的效果，在组件上添加了onClick点击事件，当用户点击该待办项时，数据isComplete的更改就能够触发UI的更新。

```
@Componentstruct ToDoItem {  @State isComplete : boolean = false;  @Builder labelIcon(icon) {...}  ...  build() {    Row() {      if (this.isComplete) {        this.labelIcon($r('app.media.ic_ok'))      } else {        this.labelIcon($r('app.media.ic_default'))      }      ...     }    ...    .onClick(() => {      this.isComplete= !this.isComplete;     })  }}
```

## 循环渲染列表数据

刚刚只是完成了一个ToDoItem组件的开发，当我们有多条待办数据需要显示在页面时，就需要使用到ForEach循环渲染语法。

例如这里我们有五条待办数据需要展示在页面上。

```
total_Tasks:Array<string> = [  '早起晨练',  '准备早餐',  '阅读名著',  '学习ArkTS',  '看剧放松']
```

ForEach基本使用中，只需要了解要渲染的数据以及要生成的UI内容两个部分，例如这里要渲染的数组为以上的五条待办事项，要渲染的内容是ToDoItem这个自定义组件，也可以是其他内置组件。

**图7** ForEach基本使用
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.40876918841066112847297183278089:50001231000000:2800:C0A4DFFA308C34669FCE98A54C43DD1CD5866F29B5502E494A882C372C2EF94D.png?needInitFileName=true?needInitFileName=true)

ToDoItem这个自定义组件中，每一个ToDoItem要显示的文本参数content需要外部传入，参数传递使用花括号的形式，用content接受数组内的内容项item。

最终完成的代码及其效果如下。

```
@Entry@Componentstruct ToDoList {   ...   build() {     Row() {       Column() {         Text(...)           ...         ForEach(this.totalTasks,(item) => {           TodoItem({content:item})         },...)       }       .width('100%')     }     .height('100%')   } }
```

**图8** ToDoList页面
![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.21738601426068546909242523085881:50001231000000:2800:ADFEE1BE900AEB41871F8C9C76AB152278976B0C75C69B9061A5D9F2C0AAB334.png?needInitFileName=true?needInitFileName=true)