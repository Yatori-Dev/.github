![yatori](https://socialify.git.ci/Changbaiqi/yatori/image?description=1&font=Inter&forks=1&issues=1&logo=https%3A%2F%2Fraw.githubusercontent.com%2FChangbaiqi%2Fyatori%2Fmain%2FREADME%2Fimages%2F1710254379397-modified.png&name=1&pattern=Diagonal%20Stripes&pulls=1&stargazers=1&theme=Dark)


<div align="center"><h1>Yatori课程助手</h1></div>


<div align="center"><img width="100px" src="https://img.shields.io/badge/Java17-passing-r.svg"></img> <img width="125px" src="https://img.shields.io/badge/Maven3.8.1-building-r.svg"></img></div>

## 📢作者有话说

> 1、因作者学业繁忙，之后的更新需要等2025年才能开始更新，不过目前所有功能都还是能用的，这点不用担心。
>
> 2、有些学校可能用仓辉的时候会卡住要么一直刷屏报错，这种情况可能是因为你所用的平台是英华套壳的，所以你只需要把刷课类型“CANGHUI”改成“YINGHUA”即可。

## 🤔问题咨询

> QQ交流群：932447008
>
> B站：[BiliBili for 长白崎](https://space.bilibili.com/36987520)（不定时更新计算机相关技术教程）
>
> 个人博客：[长白崎の个人博客 (changbaiqi.top)](https://blogs.changbaiqi.top/)
>
> 技术打赏：[赞助墙 | 长白崎の个人博客 (changbaiqi.top)](https://blogs.changbaiqi.top/sponsorWall/)

## 🎯功能支持及特性：

> - [x] 独立程序，不依赖浏览器
> - [x] AI自动识别跳过验证码
> - [x] 多账号同刷
> - [x] 支持状态邮箱通知
> - [x] 支持自动考试（目前支持英华和仓辉。别问，问就是只有人提供了仓辉和英华的账号我才能开发，没人提供其他平台账号测试我也没办法）
> - [x] 答题支撑AI大模型加持
> - [x] 灵活配置文件
> - [x] 自动继续上次记录时长刷课
> - [x] 可部署服务器
> - [x] 部分平台支持暴力模式（无视前置课程学习限制，一门课所有视屏同刷！！！）

## 🎯支持平台：

> - [x] 英华学堂（支持限制性暴力模式,支持自动考试）
> - [x] 创能平台（不支持暴力模式，支持自动考试）
> - [x] 仓辉实训（支持暴力模式，支持自动考试）
> - [x] 学习公社（目前只支持普通模式）
> - [ ] 智慧树（暂不支持，除非有人提供账号支持开发测试）
> - [ ] 盗梦空间抢活动（估计要等比较久的时间再整合了）
> - [ ] 学习通（暂不支持，除非有人提供账号支持开发测试）
>
> ==注：==英华限制性暴力模式指的是如果你学校英华平台的课程视屏没有前置视屏观看限制那么就可以开，这个前置视屏观看限制指的是，一个章节的视屏你要观看必须要先把前面章节的视屏看完才能看，这就叫做前置视屏观看限制。

## 🎉食用方式：

### 代码食用：

> 施工中...

### 直接食用:

> 下载releases然后解压修改config配置文件之后点击start.bat启动即可。
>
> 注意：填url的时候是填写学校英华的根链接，不能带uri，
>
> 比如[https://mooc.xxx.edu.com/](https://mooc.xxx.edu.com/)，而不是[https://mooc.xxx.edu.cn/xx/xx](https://mooc.xxx.edu.cn/xx/xx)
>
> 以及不能用[https://mooc.yinghuaonline.com/](https://mooc.yinghuaonline.com/)，要用自己学校的链接，比如[https://mooc.xxx.cn/](https://mooc.xxx.cn/)，每个学校的链接都不同，这个可以自己去找去问。
>
> 配置文件说明（==注意==！！！其实大部分参数可以根据需求进行省略不写，以下只是对于各参数的例子罢了！）：
>
> ```json
> {
>     "setting":{
>         "emailInform":{//邮箱通知设置
>             "sw": 0,//0代表关，1代表开
>             "smtpHost": "", //SMTP服务器地址
>             "smtpPort": "", //SMTP服务器端口
>             "email":"", //发送方邮箱
>             "password":"" //邮箱授权码或App密码
>         },
>         "aiSetting": {
>             "aiType": "CHATGLM",//目前只支持智普清言的AI，智普填CHATGLM就行
>             "API_KEY": "",//AI的API_KEY自己去智普清言官网获取（有免费余额的）
>         }
>     },
>     "users": [
>         {
>             "accountType": "CANGHUI",//指定平台，"YINGHUA"代表英华学堂（创能平台也使用这个），CANGHUI代表仓辉平台，ENAEA代表学习公社
>             "url": "url",//学习公社不用配，其他平台必须配平台主页的根url，不同学校url不同，比如https://mooc.xxx.cn/，注意千万别带uri指别写成https://mooc.xxx.cn/xxx/xxx这样。
>             "account": "账号",//账号
>             "password": "密码",//密码
>             "coursesCustom": {
>                 "videoModel": 1,//模式设定，0代表不刷视屏，1为普通模式，2为暴力模式，默认为1，暴力模式目前只支持仓辉
>                 "autoExam": 1,//是否自动考试，0代表不考，1代表考，默认为0，注意，目前自动考试只支持仓辉和英华！！！
>                 "excludeCourses": ["课程1", "课程2"],//这个参数代表需要排除不刷的课程，复制课程的名称填入即可（一字不差）
>                 "includeCourses": ["课程3", "课程4"],//这个指的是需要刷的课程，如果不填默认刷全部课程除非设置了排除课程
>                 "coursesSettings": [
>                     {
>                         "name": "大学生劳动教育", //对应需要单独需要客制化的课程名称
>                         "includeExams": ["试卷名称1","试卷名称2"],//对应课程需要考试的试卷名称
>                         "excludeExams": ["试卷名称3","试卷名称4"],//对应课程不需要考试的试卷名称
>                     }
>                 ]
>             }
>         }
>     ]
> }
> ```
>
> 刷课支持多账号，根据需求自行进行改动。
>
> 示例1：
>
> ```json
> {
> "users": [
>   {
>       "accountType": "YINGHUA",
>       "url": "张三的url",
>       "account": "张三的账号",
>       "password": "张三的密码"
>   },
>   {
>       "accountType": "CANGHUI",
>       "url": "李四的url",
>       "account": "李四的账号",
>       "password": "李四的密码",
>       "coursesCustom": {
>           "videoModel": 2,
>           "autoExam": 1
>       }
>   }
> ]
> }
> ```
>



## 🗣项目说明：

> 以后项目将会分三个版本模块
>
> 1、yatori-core
>
> 2、yatori-console
>
> 3、yatori-web

### yatori-core

> 这个是给开发者用的，也是所有yatori衍生产品的核心，里面提供了刷课的API函数调用接口。
>
> 目前最新发布的是1.0.0-beta。2
>
> 不过目前项目暂未完善，所以也不需要急着引用开发。
>
> yatori-core也已经上线Maven中央仓库，直接Maven引入即可
>
> ```xml
>      <dependency>
>          <groupId>io.github.changbaiqi</groupId>
>          <artifactId>yatori-core</artifactId>
>          <version>1.0.0-beta.2</version>
>      </dependency>
> ```

### yatori-console

> 这个是基于yatori-core的衍生产品，也是可以直接使用的控制台版本，目前最为完善的可直接使用版本。在release里面下载即可。

### yatori-web

> 这个是基于yatori-web的衍生产品，也是可以直接使用的可视化Web控制版本，目前暂未开发好。暂时也还用不了。

## 免责声明：

> 代码已开源，程序只供学习使用，严禁贩卖，若对贵公司造成损失立马删库（保命(doge)）。

## 贡献者 
<a href="https://github.com/Changbaiqi/yatori/graphs/contributors">   <img src="https://contrib.rocks/image?repo=Changbaiqi/yatori" /> </a>

## 鸣谢

> 感谢[**JetBrains**](https://www.jetbrains.com/zh-cn/community/opensource/#support)提供的开源开发许可证，JetBrains 通过为核心项目贡献者免费提供一套一流的开发者工具来支持非商业开源项目。
>
> <img src="./README/images/jetbrains-variant-3.png" alt="jetbrains-variant-3" width="200px" />

[![Stargazers over time](https://starchart.cc/Changbaiqi/yatori.svg?variant=adaptive)](https://starchart.cc/Changbaiqi/yatori)