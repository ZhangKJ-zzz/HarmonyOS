# 运行Hello World

## 下载与安装DevEco Studio

在HarmonyOS应用开发学习之前，需要进行一些准备工作，首先需要完成开发工具DevEco Studio的下载与安装以及环境配置。

进入[DevEco Studio下载官网](https://developer.harmonyos.com/cn/develop/deveco-studio)，单击“立即下载”进入下载页面。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104602.90306589229674463941403592221986:50001231000000:2800:1D9F372576D6B26CDD1EF22E283E1C030964B8127F2B3BE92FFB2E7D977A577B.png?needInitFileName=true?needInitFileName=true)

DevEco Studio提供了Windows版本和Mac版本选择，可以根据操作系统选择对应的版本进行下载。

这里以Windows为例进行安装。

下载完成后，双击下载的“deveco-studio-xxxx.exe”，进入DevEco Studio安装向导，在如下界面选择安装路径，默认安装于“C:\Program Files”下，也可以单击“Browse...”指定其他安装路径，然后单击“Next”。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.01449195393346222853929431894676:50001231000000:2800:81B88BBC1771E1F929A98D19A31B0E22B328D83A037810F5AC2474F69770EE40.png?needInitFileName=true?needInitFileName=true)

如下安装选项界面勾选DevEco Studio后，单击“Next”，直至安装完成。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.70155722447275127540939260187536:50001231000000:2800:F81228561B4C7FF09222BF175979A8345C43ACE36B5E0A96EEE9BF2BEB62D4DB.png?needInitFileName=true?needInitFileName=true)

安装完成后，单击“Finish”完成安装。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.87184778857610132715396291425092:50001231000000:2800:B932AFA12E468445975FF77DFF9AEDE589AC49EDD885881A306F57A6389370B4.png?needInitFileName=true?needInitFileName=true)

## 配置环境

双击已安装的DevEco Studio快捷方式进入配置页面，IDE会进入配置向导，选择Agree，同意相应的条款，进入配置页。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.67653841931983966908577872052870:50001231000000:2800:ACA54EFA82238C36537A4D27987E138BE35F94873F5A1724A2FB490C7C7BF00B.png?needInitFileName=true?needInitFileName=true)

进入DevEco Studio配置页面，首先需要进行基础配置，包括Node.js与Ohpm的安装路径设置，选择从华为镜像下载至合适的路径。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.89145178002211512054306859412656:50001231000000:2800:EC46EF70807484C401B34CE36FA15DB0E9E9F1C48D237D17E4A412AE899342DE.png?needInitFileName=true?needInitFileName=true)

单击'Next'进入SDK配置，设置为合适的路径，

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.74090595054404208643036522028618:50001231000000:2800:92EA5E7CFABBE80539332F98A05828D3EEDD8CFB423C18DFF56AAB70B299F3E9.png?needInitFileName=true?needInitFileName=true)

点击'Next'后会显示'SDK License Agreement'，阅读相关协议后，勾选'Accept'。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.99255624775903661454229082197943:50001231000000:2800:191CB564AD8BE22BA39F9C5B8143013243A12D524E3E5CF4332773695CBFC2B3.png?needInitFileName=true?needInitFileName=true)

单击‘Next’进入配置预览页，在这里进行配置项的确认。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.26970565164518323884719310054419:50001231000000:2800:3E763D13A9049FEB21700A247C67F1FA03620079CB19D7EDBB9B9E56706F0494.png?needInitFileName=true?needInitFileName=true)

确认完成后，单击'Next'，进入下一步。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.38465626072890544440060740725015:50001231000000:2800:612D7E89A3D3C1E01D766670F9814A933545EB6B7E9D07D0F7BEEC1CDB509E72.png?needInitFileName=true?needInitFileName=true)

等待配置自动下载完成，完成后，单击'Finish'，IDE会进入欢迎页，我们也就成功配置好了开发环境。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.14888129437929502192986808631667:50001231000000:2800:F743EC985E98EDBF3E8685EC73D886534B9B85AFC7F056515F7F6C866F5D9421.png?needInitFileName=true?needInitFileName=true)

准备工作完成后，接下来将进入DevEco Studio进行工程创建和运行。

## 创建项目

如果你是首次打开DevEco Studio，那么首先会进入欢迎页。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.29253328215314610406721735763623:50001231000000:2800:17D75AB0B1E951445040C843A1F41A601D6505614DA60141784431DD6AB9F062.png?needInitFileName=true?needInitFileName=true)

在欢迎页中单击Create Project，进入项目创建页面。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.82831572314508065638304162425570:50001231000000:2800:FD4F8A50BCC25D15533190EBD6A8D3E6F63E8F2422F99134C89B08D852435959.png?needInitFileName=true?needInitFileName=true)

选择‘Application’，然后选择‘Empty Ability’，单击‘Next’进入工程配置页。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.21227811129180483346889978867252:50001231000000:2800:3224D1F794669BE3D494C97CE4D14D9D7707299654597038878E69D934F737CF.png?needInitFileName=true?needInitFileName=true)

配置页中，详细信息如下：

- Project name是开发者可以自行设置的项目名称，这里根据自己选择修改为自己项目名称。
- Bundle name是包名称，默认情况下应用ID也会使用该名称，应用发布时对应的ID需要保持一致。
- Save location为工程保存路径，建议用户自行设置相应位置。
- Compile SDK是编译的API版本，这里默认选择API9。
- Model选择Stage模型，其他保持默认即可。

然后单击“Finish”完成工程创建，等待工程同步完成。

## 认识DevEco Studio界面

进入IDE后，我们首先了解一下基础的界面。整个IDE的界面大致上可以分为四个部分，分别是代码编辑区、通知栏、工程目录区以及预览区。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.42851636166607295576572946278524:50001231000000:2800:AA4F660BA2C9DE629E5FF7D15973F1EAB13B7001AD7A8C7106D0990033B02B46.jpg?needInitFileName=true?needInitFileName=true)

1. 代码编辑区

   中间的是代码编辑区，你可以在这里修改你的代码，以及切换显示的文件。通过按住Ctrl加鼠标滚轮，可以实现界面的放大与缩小。

2. 通知栏

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.69280364573134341221907084872959:50001231000000:2800:380383867E408B5D4E26C95C18CA863BE9B26BCBE200481EEBB3E50B3291DE18.png?needInitFileName=true?needInitFileName=true)

   在编辑器底部有一行工具栏，主要介绍常用信息栏，其中Run是项目运行时的信息栏，Problems是当前工程错误与提醒信息栏，Terminal是命令行终端，在这里执行命令行操作，PreviewerLog是预览器日志输出栏，Log是模拟器和真机运行时的日志输出栏。在后续使用中会陆续接触。

3. 工程目录区

   左侧为工程目录区，后续章节会详细介绍。

   ![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.55413586768756141108471861276862:50001231000000:2800:13433DD6954800CBA29D3F8384C5B240B8F5AAE973B231A2A3124A2E9BCB3AC8.png?needInitFileName=true?needInitFileName=true)

4. 预览区

   单击右上角Previewer，可以预览相应的文件UI展示效果。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.99153498539039229169630069681669:50001231000000:2800:C1BE5C632766CF5A3A5F605B4502C13F4937DDD759E514779FBAB8A28603CE77.png?needInitFileName=true?needInitFileName=true)

   预览器提供了一些基本功能，包括旋转屏幕，切换显示设备及多设备预览等。单击旋转按钮，可以切换竖屏和横屏显示的效果。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104603.67061807926959468982597314631394:50001231000000:2800:32D62FC0F064CE9BE49596B60F5550803A13B6982DD099C4AC7BC3B38C973701.png?needInitFileName=true?needInitFileName=true)

   也可以单击如下列表按钮，切换显示的设备类型。弹出框内会显示Available Profiles，即可用的设备类型。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.42413077906585804606683804321870:50001231000000:2800:345D2A06B28200E0B4A5EE3FA099E71706A91D128251F90E67A8E0FDA0F143BC.png?needInitFileName=true?needInitFileName=true)

   如单击Foldable切换设备，也可以单击旋转按钮切换Foldable的横竖屏显示模式。

   打开Muti-profile preview开关，可以实现多个尺寸设备的实时预览。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.86346282488193798337439701648152:50001231000000:2800:A991027E59978AE6687A3F685BA73B5B5CC0BD2FE4A4AF124D5ED2CBCDEDE101.png?needInitFileName=true?needInitFileName=true)

   单击预览器右上角组件预览按钮，可以进入组件预览界面。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.13884554801629013885810382667899:50001231000000:2800:11242BCA833C15099A8804990A592EBAC52B95141A05A25F83810433AD674E9E.png?needInitFileName=true?needInitFileName=true)

   组件预览模式可以预览当前组件对应的代码块。

   点击相应组件，代码文件中会框选对应的组件代码部分，下方则对应当前组件的基本属性。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.10997629578888829861468262549453:50001231000000:2800:C6935F4C9FFBEC6A435D601778AF94EF1B9DC13A96B2DE26D59CD04E1DEDAEAD.png?needInitFileName=true?needInitFileName=true)

## 运行Hello World

IDE提供了本地模拟器供开发者使用，我们首先需要下载安装本地模拟器，然后进行运行工程。

1. 单击顶部工具栏Tools>Device Manager。

   ![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.61300158347172671533345037902927:50001231000000:2800:C6B3C4E2CA4FEA57191AAD67B4789F00A41EDB3ABDE63449AB70B9F375A7FFF1.png?needInitFileName=true?needInitFileName=true)

2. 选择Local Emulator，设置合适的Local Emulator Location存储地址，然后单击’+New Emulator’。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.42428920419987175045619176273487:50001231000000:2800:EC2CC1684B56C63502EF8EB8AE347C9AC19AD394EECA2DF6BAA957BA2363AAA8.png?needInitFileName=true?needInitFileName=true)

   选择Huawei_Phone手机模拟器，单击'Next'，进入模拟器系统下载页。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.51644591962553868000504401789895:50001231000000:2800:32A3A1670696BCA3DEBB56026F467722234156E1A3057FF0CDF3A9CE6640266D.png?needInitFileName=true?needInitFileName=true)

   选择下载api9的系统镜像，然后单击'Next’，等待下载完成。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.44066569528808060680829343617287:50001231000000:2800:E64563BC12DF50FC5DC9446150AA5395AF7240E752389C2632F8EDF24C512EBC.png?needInitFileName=true?needInitFileName=true)

   下载完成后，进行创建相应的手机模拟器，单击Finish完成创建。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.17441570854847136576642778421938:50001231000000:2800:A92114A200A8566BF595562B6F07FE9B58FCC4E4C5BA8FED868AD67715D5279E.png?needInitFileName=true?needInitFileName=true)

   下载完成后，在Local Emulator页面中会出现创建的手机模拟器，点击Actions按钮，就能够启动模拟器。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.33667244673159681328150204281626:50001231000000:2800:5D60D5B3A3D49043A461E7F5D485CCAEDE7F7606BED6BEB1F07624FB678E8C95.png?needInitFileName=true?needInitFileName=true)

   模拟器启动后，点击上方启动按钮，将Hello World工程运行到模拟器上。

   ![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.04580399628573176206342100885478:50001231000000:2800:A5A29527F5139197E77505F6CBF3F933606509B5C5C20E0AB0B194A87A856CB9.png?needInitFileName=true?needInitFileName=true)

   IDE构建完成后，即可在模拟器上看到运行效果，我们也就完成了Hello World工程在模拟器上的运行。

   ![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.58036340529962919747699433450359:50001231000000:2800:806874CD45069AA963E148C6C8E6FC6FF28D47F572CC93FFE5156980346AE211.png?needInitFileName=true?needInitFileName=true)

## 了解基本工程目录

### 工程级目录

工程的目录结构如下。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.97681025267574018823684782464195:50001231000000:2800:4AB533C93118CD98CF8E84EE61A0BA68AB7616F38D298A73E2EB414B9ED885D0.png?needInitFileName=true?needInitFileName=true)

其中详细如下：

- AppScope中存放应用全局所需要的资源文件。
- entry是应用的主模块，存放HarmonyOS应用的代码、资源等。
- oh_modules是工程的依赖包，存放工程依赖的源文件。
- build-profile.json5是工程级配置信息，包括签名、产品配置等。
- hvigorfile.ts是工程级编译构建任务脚本，hvigor是基于任务管理机制实现的一款全新的自动化构建工具，主要提供任务注册编排，工程模型管理、配置管理等核心能力。
- oh-package.json5是工程级依赖配置文件，用于记录引入包的配置信息。

在AppScope，其中有resources文件夹和配置文件app.json5。AppScope>resources>base中包含element和media两个文件夹，

- 其中element文件夹主要存放公共的字符串、布局文件等资源。
- media存放全局公共的多媒体资源文件。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.36501621348626478525499831421132:50001231000000:2800:FCE7AD12DBCFA6D9AD0534A938BFFB97A44141C1D217644F6C79204DB2E7A246.png?needInitFileName=true?needInitFileName=true)

### 模块级目录

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.45983065067585771968858961116363:50001231000000:2800:A00E937F7CBE13098C4EA85781B4F01A618AE6A04BF34C28BC34D96934663BB7.png?needInitFileName=true?needInitFileName=true)

entry>src目录中主要包含总的main文件夹，单元测试目录ohosTest，以及模块级的配置文件。

- main文件夹中，ets文件夹用于存放ets代码，resources文件存放模块内的多媒体及布局文件等，module.json5文件为模块的配置文件。
- ohosTest是单元测试目录。
- build-profile.json5是模块级配置信息，包括编译构建配置项。
- hvigorfile.ts文件是模块级构建脚本。
- oh-package.json5是模块级依赖配置信息文件。

进入src>main>ets目录中，其分为entryability、pages两个文件夹。

- entryability存放ability文件，用于当前ability应用逻辑和生命周期管理。
- pages存放UI界面相关代码文件，初始会生成一个Index页面。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.38136443291134648748631050435720:50001231000000:2800:B4447033473CF68A9F82BBF768EC3B75B02DA06C4ED71295D0D1FDDA050F1E09.png?needInitFileName=true?needInitFileName=true)

resources目录下存放模块公共的多媒体、字符串及布局文件等资源，分别存放在element、media文件夹中。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104604.70326380326145607518508122080549:50001231000000:2800:E0FFD4C3F0C91BAC38396AB7FC2A24474777EAC46F92DA2F059AA43D85DD7F11.png?needInitFileName=true?needInitFileName=true)

### app.json5

AppScope>app.json5是应用的全局的配置文件，用于存放应用公共的配置信息。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.29931087071694403485882979272398:50001231000000:2800:C59F0A1E42FF656386CFCA00E74232CA97364E084A969F8DB26885157E81C908.png?needInitFileName=true?needInitFileName=true)

其中配置信息如下：

- bundleName是包名。
- vendor是应用程序供应商。
- versionCode是用于区分应用版本。
- versionName是版本号。
- icon对应于应用的显示图标。
- label是应用名。

### module.json5

entry>src>main>module.json5是模块的配置文件，包含当前模块的配置信息。

![img](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.38682806193879465925751958320534:50001231000000:2800:FAD62103111C02F18138D7A0C57DBAA970AD4BD0414190E27484762959664698.png?needInitFileName=true?needInitFileName=true)

其中module对应的是模块的配置信息，一个模块对应一个打包后的hap包，hap包全称是HarmonyOS Ability Package，其中包含了ability、第三方库、资源和配置文件。其具体属性及其描述可以参照下表1。

| 属性                | 描述                                                         |
| ------------------- | ------------------------------------------------------------ |
| name                | 该标签标识当前module的名字，module打包成hap后，表示hap的名称，标签值采用字符串表示（最大长度31个字节），该名称在整个应用要唯一。 |
| type                | 表示模块的类型，类型有三种，分别是entry、feature和har。      |
| srcEntry            | 当前模块的入口文件路径。                                     |
| description         | 当前模块的描述信息。                                         |
| mainElement         | 该标签标识hap的入口ability名称或者extension名称。只有配置为mainElement的ability或者extension才允许在服务中心露出。 |
| deviceTypes         | 该标签标识hap可以运行在哪类设备上，标签值采用字符串数组的表示。 |
| deliveryWithInstall | 标识当前Module是否在用户主动安装的时候安装，表示该Module对应的HAP是否跟随应用一起安装。- true：主动安装时安装。- false：主动安装时不安装。 |
| installationFree    | 标识当前Module是否支持免安装特性。- true：表示支持免安装特性，且符合免安装约束。- false：表示不支持免安装特性。 |
| pages               | 对应的是main_pages.json文件，用于配置ability中用到的page信息。 |
| abilities           | 是一个数组，存放当前模块中所有的ability元能力的配置信息，其中可以有多个ability。 |

对于abilities中每一个ability的属性项，其描述信息如下表2。

| 属性                  | 描述                                                         |
| --------------------- | ------------------------------------------------------------ |
| name                  | 该标签标识当前ability的逻辑名，该名称在整个应用要唯一，标签值采用字符串表示（最大长度127个字节）。 |
| srcEntry              | ability的入口代码路径。                                      |
| description           | ability的描述信息。                                          |
| icon                  | ability的图标。该标签标识ability图标，标签值为资源文件的索引。该标签可缺省，缺省值为空。如果ability被配置为MainElement，该标签必须配置。 |
| label                 | ability的标签名。                                            |
| startWindowIcon       | 启动页面的图标。                                             |
| startWindowBackground | 启动页面的背景色。                                           |
| visible               | ability是否可以被其他应用程序调用，true表示可以被其它应用调用， false表示不可以被其它应用调用。 |
| skills                | 标识能够接收的意图的action值的集合，取值通常为系统预定义的action值，也允许自定义。 |
| entities              | 标识能够接收Want的Entity值的集合。                           |
| actions               | 标识能够接收的Want的Action值的集合，取值通常为系统预定义的action值，也允许自定义。 |

### main_pages.json

src/main/resources/base/profile/main_pages.json文件保存的是页面page的路径配置信息，所有需要进行路由跳转的page页面都要在这里进行配置。

![点击放大](https://alliance-communityfile-drcn.dbankcdn.com/FileServer/getFile/cmtyPub/011/111/111/0000000000011111111.20240111104605.61576995654892097280213653266093:50001231000000:2800:40B75A119CA59588F1CCE504DB28B45726D8991C86E9AA0A17A719ABA48DD292.png?needInitFileName=true?needInitFileName=true)

## 参考链接

- DevEco Studio下载与安装：[DevEco Studio下载与安装](https://developer.harmonyos.com/cn/docs/documentation/doc-guides/software_install-0000001053582415)
- 配置开发环境：[配置开发环境](https://developer.harmonyos.com/cn/docs/documentation/doc-guides/environment_config-0000001052902427)