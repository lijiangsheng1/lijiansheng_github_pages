---
categories:
- 开源
- 感悟
date: 2016-08-25T09:50:51+08:00
description: ""
keywords:
- Open Source
- Culture
- Cloud comuting
title: 为什么说扁平化的组织结构是治愈劣根性的良方
url: ""
draft: true
---

# 缘起

我是开源的布道师，也是某些人文方面的思考者、研究者。开源将成为最后的软件生产模式，社区人将会是自由人，这样一个终结的命题眼看着就要成为现实。然而，我自己在现实中是非常[失败][^1]的，失望之余就是在反思。

昨日正好有一篇某同事曝光／吐槽“冯大辉”的文章发出，全文如下：

> ## 冯大辉到底是不是技术大牛？ 一个程序员眼中的 Fenng

> 匿名：丁香园码农一枚。

> 现在看大辉的朋友圈，称呼他CTO，他都会愤怒，言下之意是他何止是CTO。从我的角度来说，他在丁香园期间扮演的确实不是CTO，他可以说是丁香园的“首席产品体验师”，也可以说是“首席邮件挑错师”，就是不能说他是CTO。听说大辉要自己创业了，从一个程序员角度看，我最想说的是“希望他能尽快找到一个靠谱的CTO”

> 在丁香园写代码时间并不短，说一下我知道事情，确切的说是我理解的事实，因为也不是最早加入的，有些事儿是听公司老程序员说的。

> 大辉在丁香园工作期间，保持非常高的微博、微信朋友圈和公众号更新频率，你去看他的timeline，有些天几乎是平均几十分钟一条。作为一个不愿打断编程思路的程序员，我开始的时候很难理解他作为CTO是如何工作的。

> 后来也慢慢了解了，因为他在丁香园任职CTO，一行代码都没有写过，一行都没有。

> 更加奇怪的是，他也从来不做Code Review，从来不做。

> 他在丁香园也同时管理产品团队，但据我所知，他从来没有实际参与过任何一个产品的原型设计，需**审也基本不参加。

> 你可能觉得一个管理岗位，何须亲自写代码、Code Review和需**审呢？可大家不要忘了，他加入丁香园是在丁香园刚刚完成A轮融资以后，整个公司也不到100人，技术产品加起来也就20多人吧。

> 一个A轮公司的CTO不去了解公司产品和技术的架构正常，不深入技术细节做技术决策正常吗？

> 事实上在这几年我们遇到的各种问题：有架构规划上，有数据库的，有技术选型的，有性能优化的，他一边对外写着介绍Facebook/Twiiter等流行互联网公司的技术架构科普文章，在技术圈内博取技术大牛的名声；另一边却在公司从未亲自带领团队去解决这些问题，他常说的一句话：对我们最好的培养就是丢一大堆问题给我们解决。最后技术架构一团糟，大辉却叉着腰把所有的责任推给公司，推给一线程序员，唯独他作为业界技术大牛，却不需要为技术架构的问题承担责任。

> 很早以前，丁香园就上马过问答项目，完全是撞大运的心态，根本没有完整的运营思路，最好笑的是，这个项目一个程序员离职以后，公司无人能够接手这个项目，要让人接手，就必须先“重构代码”。这种才开始就要重构代码的事情在后来经历了很多次，包括后来公司非常重要的丁香云管家项目。

> 说起云管家这个项目，先是从外面请来了一个“首席科学家”，大家都以为很厉害的样子。结果呢？这个首席科学家非要用Redis做底层的数据持久化存储，美其名曰：“微博就是用Redis存储的”，期间很多研发同事都不同意，都快吵翻了，但是他是大辉任命的首席科学家，大辉也从来不管技术选型这种“小事情”，而是忙着写微信公众号发微博。

> 所幸后来有人来替他擦了这个屁股，罢免了“首席科学家”，替换掉了Redis，改回了MySQL数据库，云管家项目才得以顺利上线和运营。

> 关于整个公司的技术架构和选型，作为一个程序员我是从来没有看见大辉做过这种事情，也从不组织这种讨论，完全是随着各个团队自己搞，各种编程语言、各种框架，各种版本随便程序员自己用，这给很多项目埋下了坑，这些坑到后来都演变成各种冲突和矛盾。

> 说到团队培养问题。这几年，我有印象的，总共大约请过4-5个人来公司培训，基本上也没有太多规划，以他的好友为主。日常团队内部的技术交流完全靠团队小Leader自己搞，有一搭没一搭，你还不能抱怨，一抱怨他就要到朋友圈不阴不阳的说“现在的年轻人总是抱怨培训不够，你代码一堆bug，公司那么多问题没有解决，解决这些问题不就是最好的培训吗？”。

> 可是你是CTO啊，在资源永远不够，别人解决不了的情况下，你倒是给我们指点一下方向，规划一下架构，判断一下解决方案，决策一下技术选型啊？对于这样的业界技术大牛，我们解决不了的问题，对你来说，不就是很轻松搞定的问题吗？你有时间发朋友圈和微博给大家所谓示范如何利用社交媒体，就没有时间亲身示范一下如何写代码吗？哪怕你是DBA出身，给我们示范一下如何调优SQL语句，程序员怎样注意和避免SQL注入漏洞也好呀，但只是骂，从来没有亲自示范。

> 以前在另外一家初创型公司工作，CTO都是碰到问题，团队解决不了的时候，自己亲自上阵的，这个能力在大辉身上是没有的，他只有逼急了骂人。

> 看见他在外面和别人互喷吵架，总是想，那么多时间精力用到我们自己的开发和产品上多好呢？而他在外界和人互喷，最大的资本就是这几年丁香园产品发展的不错，一副“老子有后面的产品做背书，你们能说我只是会喷吗？”

> 现在他离职了，不停给外界传递丁香园过去很多重要的成绩都是他带来的。可是，对于一直参与产品研发的同事会认同吗？

> 公司面向企业的业务是收入的主要来源，这部分业务他根本就不关心，还总是设置各种障碍，总之在他眼里这些做企业业务的人都是笨蛋，根本不值得尊重，公开和私下里经常说一下很难听的话来攻击团队同事。这些行为直接导致了公司团队的矛盾，也和公司的文化格格不入，在朋友圈喷，在公众号含沙射影，就是不愿意面对面坦诚交流，以“开会都是浪费时间”的名义。

> 在移动方面，丁香园做的最成功的就是快速移动转型，现在的日活非常高的用药助手App几乎是这个领域最好的应用，而丁香园和丁香医生系列微信公众号更是在微信上有巨大的影响。

> 用药助手App的创意是天天老板在海外参会看到美国用药助手（名字忘了）在美国上市，回国后迅速召集团队讨论，然后大家都尊敬的叮当叔挑起产品大梁，团队迅速研发，踩上了App的红利期，产品迅速走红，并且带来了公司B轮融资。

> 而微信公众号，丁香园大号最开始一直都是CEO张老板用一己之力写出了大几十万粉丝后来交给团队处理，丁香医生系列号则是大众医学传播团队的巨大贡献。据我所知，大辉从来都不参加丁香医生微信号的工作例会，从来都不参加，从来都不。

> 这个团队在初太医的带领下，帮公司在大众传播领域开了一个很好的头，公司内部的同事一度都认为丁香医生就说丁香医生微信公众号。

> 然后是公司目前重点投入的“来问医生”，说起来更是有趣。大辉在外面说这个产品是买来的，实际上呢？实际上是团队没日没夜关小黑屋封闭开发出来。他买来的那些代码根本就没法维护，完全无法用。要使用的话，就必须和原来掉过无数次的坑一样，必须全部停下业务来重构。现在我们技术团队一说重构这个词，业务部门就头大。

> 在丁香园的产品和技术都有一个体会，大辉总是时不时的喊“我们太慢了，我们要快”，但是怎么快呢？谁知道呢？喊完以后有什么用呢？作为一个已经早早脱离技术的管理者，只知道召集所有人半夜喊几句，或者在群里骂几句，看周报主要是标点、大小写和错别字等等，有一次他把另外一个同事的周报猛夸了一阵，而这个同事一直被数个业务部门投诉。

> 丁香园的程序员们都知道：大辉根本就不管技术团队，也不懂编程，他只管产品经理，丁香园从技术层面我想不会有哪个程序员会认同他做了什么实际贡献。而谈到管理，研发体系的梳理和完善是从范凯老师来丁香园以后开始的吧。与医疗行业的其他公司比，过去丁香园在技术领域还不至于落后，或者说有一些领先，其实是因为陈良、文磊等真正的一批优秀的骨干工程师在顶着，大辉总是高估了自己，低估了别人。

> 丁香园的技术实力，与丁香园品牌和医生资源等是不匹配的，我觉得技术是拖了后腿的，丁香园本可以用互联网中上的技术实力加上丁香园过去积累的品牌和资源跑的更快。现在丁香园只能说比那些更烂的团队要好。

> 如果说从大辉身上学到了点什么，那就是如何喷人吧，怎么喷同事，怎么喷同行，怎么喷很多其实和我们毫无关系的人和事，然后感叹时间不够用，应该把时间用在“美好的事情”上。

> 张小龙曾经说过“要提防那些blog写得好的产品经理，因为在blog上花的时间越多，在产品上花的时间就越少。原来还以为有例外，现在看起来无一例外。”

> 我想说，这句话要是用在CTO身上更加合适，在朋友圈、微博和公众号上花的时间越多，在真正技术上花的时间就越少，这个绝无例外。无论是技术精进和管理能力，我再也不会相信，把大量时间耗费在社交媒体上和人互喷的人能够做好。

> 最后，听说大辉要自己创业了，我最想说的是“希望他能尽快找到一个靠谱的CTO”。

> 关于一些其他不太好说的事情就不说了，希望大辉能够像自己表现的那样，有尊严一点吧，别做那些让兄弟们不好意思说的事情了。

> ## Feng 高效的一天

> 不混圈子，不到会议上换名片，不接受媒体采访，每天工作超过12小时。理解他的一天，才知道什么叫比你聪明的人比你更努力，也会对精益创业和增长黑客有更深入的了解。

> 他是文学爱好者，和路遥一样，他的早晨是从中午开始的，看似平凡人生，其实百年孤独。

> 睡到11点起床，发一条朋友圈「特么的楼上装修的真是烦死人，不干扰他人这么简单的事情，在这个社会到底有多难？」

> 下楼买早餐，发一条朋友圈「我说你们这些创业者啊，一天到晚要改变世界，谁特么能来改变一下我吃早餐的环境，一个可靠的早餐能做好，才能改变世界，别特么尽搞些VR、大数据、人工智能这些不靠谱的。」

> 12点，到公司，助理忘了给他买咖啡，骂一句「你这个蠢货，滚」然后开始刷朋友圈微博，同时收发工作邮件，大约100多封吧（扁平化管理嘛），其实大部分直接删掉不看。

> 13点了，还没有吃中饭，发一条朋友圈「吃饭真是一个麻烦的事儿，浪费时间」

> 14点，开始写微信公众号，扫地的阿姨从他的办公室窗前走过，他愤怒的去拉下窗帘，发一条朋友圈「把办公环境弄好一点，比特么给员工发生日祝福重要的多」。还可以补一条「你们这些蠢货，就不能干点正经事情吗？我说了多少次了，把我办公室的窗帘和膜贴好，干不好，全特么给我滚蛋！」

> 15点，微信公众号文章有个大致的草稿了。发一条朋友圈「总有人问我每天发那么多朋友圈和微博，写公众号文章，我到底什么时候工作。他们不知道，对他们来说写一篇文章发朋友圈要耗费太多时间，对于我来说就是抬抬手指的事情。」

> 期间参加一个工作会议，大部分时间在刷手机，突然抬头说一句「停一下」，到白板前涂涂画画，骂一下人太蠢什么的，然后散会！

> 16点，断断续续修改一下公众号文章，在几个「我们都是老炮儿基友别人都是傻逼群」内交换一下八卦，互相吹捧，间或发几条朋友圈表示兄弟我虽然只在方寸之室，但天下之事无所不知，你们不要小看更不要得罪我哟。

> 17点，发一条大意如下朋友圈「关于**事情，那么多媒体发文章都没说到点上，难怪你们这些媒体都混不下去了，我要不要晚上发一篇说一下这个事情呢？」，其实文章一个下午七七八八的已经基本准备好了。文章如果是跟热点，一定是「独特视角」来写，比你们这些媒体和自媒体不知道高到那里去了；如果不是热点一般会顺便说「我写文章不喜欢跟热点，而是写那些放在时间长河中随时读起来也有价值的那种」


> 18点，开始高效率的工作。回复邮件「怎么周报中有错别字？产品经理连周报都写不好，能做的好产品吗？」「周报写的很好，大家看看他周报的排版」「麻烦大家写周报的时候都顶格写」，发各种别人发是鸡汤，他发是哲理的朋友圈「会议是效率的杀手」「一个说要为互联网献身的求职者，特么的居然问我邮箱地址是什么，他还是踏踏实实在大公司上班吧」……

> 19点，发这样的朋友圈「你们这些人，说要请我吃海底捞的，全特么都是打嘴炮」「这周已经是第三次吃海底捞了，请我吃海底捞的融资都成功了，你们感受一下」

> 20点，「海底捞的CEO就特么应该到在行约一次我，系统太特么烂了，改进一下，至少节省20%的人工，不约我，我才不告诉他，是他的大损失，本消息同时抄送微信团队」

> 21点，对微信公众号文章进行最后的润色修改，然后推送，居然发现有错别字。作为完美主义者必须发一条说明「错别字啊，真是自己很难看出来，真想花钱雇人专门帮我修改，愿意的人发个消息给我吧，不一定给你发工资，但是保证你会有惊喜」，吹捧和互动开始了，忙一阵，打赏的鼓励，质疑的拉黑。

> 22点，开始焦虑，好像同事们也都是和他一样，这一天就是在社交媒体上高效工作，具体的事儿没进展。然后让助理在团队群内发消息「所有同事，今晚11点请全部到公司开会，不得请假。」

> 23点，人头攒头，「你们可能以为我疯了，深更半夜找大家来开会，但是我真的很焦虑，我们太慢了，我们这样是干不过竞争对手的，我们必须快，你们明白我的意思吧？」

> 0点，发一首代表鉴赏逼格的歌曲到朋友圈，或许可以顺带吐槽一把「虾米就算产品再好，但我就是讨厌他们创始人的德行」，不服你来咬我啊。

> 1点，发一条「死后自会长眠，我也没打算活到80岁」，然后开始长达8小时以上的睡眠。

> 以上纯属虚构写作，切勿对号入座。


>## 这种问题就是他心中的痛。

> 因为博客写的好，自我经营的好，他的名字前面加了很多著名、首席之类的头衔，让业界对他在阿里的级别产生了很多联想。

> 但是，

> 如果有人问冯大辉「你在阿里的时候是P几啊？」

> 他一般都讳莫如深，浅浅笑一下「不高，不高……」，一种过去的荣耀不要再提的谦虚劲，给人想象空间。

> 事实上，是真的不高。

> 为什么级别是他心中的痛呢，因为他经常在江湖上和人互喷，别人质疑他的一种主要观点就是「你除了会喷以外，还有什么样的真本事？」，阿里的高级别就是「真本事」的最好背书，然而他并没有

读完这篇文章之后，我的第一反应是写此文的人，受民间文化洗礼太过于浓厚，视野太过于狭窄，凭yy将人说的一无是处。而且，按照传统文化来说，此人是属于背叛者行列，如果Feng以前原来将他当朋友的话。

那么我就产生了很多想法。也反思自己，未来该如何在本土处理这些问题。

## 什么是劣根性

劣根性，是鲁迅先生的话语。这里的概念要简单一些。仅技术本身而言。是指历代的那些民间艺人，信奉“教会徒弟饿死师傅”“留一手”“”的那些人。



## 该如何治理



[^1]: 此处的失败是需要解释一下的，我指的是我去年尝试创业之前的建立团队的失败。
