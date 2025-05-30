# 第 2.2 节 Linux 败局与 FreeBSD 败局


## Linux 败局

> **技巧**
>
> 建议先阅读原文：[还有人记得 Linux 之前，那个理想又骄傲的 BSD 吗？](https://my.oschina.net/u/5324949/blog/5434988)、[FreeBSD 大败局](https://my.oschina.net/oscpyaqxylk/blog/5457229)，然后再来阅读本文。

看过我上一篇文章《Linux 社区已经成为了一个肮脏的泥潭》以及上上一篇文章《Linux 与苦难哲学》的读者都知道，Linux 从开发者到社区乃至于用户都是充斥着难以言表的一种骄傲。仿佛自己是真正的 UNIX 后裔，是开源界的唯一真理，谁拥有 Linux，谁会 Linux，谁就掌握话语权。

如此过了三十余年，物是人非，当初的 Linux 走到了今天这个地步，无论从何种意义上来说，都是一种错位。

王垠过去写了一篇 Linux 劝进文——完全用 Linux 工作，后又发了一篇 Linux 劝退文——谈 Linux，Windows 和 Mac。人的认识是一个螺旋式上升的过程，当初的错位必将在日后得到修正。Linux 也如是。

不断的有 Arch Linux 用户到处宣传 Arch Linux 的优美。是啊，如此优美的一个系统！Nano，Vi 都依赖 Glibc，不更新就意味着你用不了这些再基础不过的基础软件，强制性地要求你更新，他们才不在乎更新会不会导致你的系统挂掉——反正我又不能给你蓝屏。我不知道这些 Arch Linux 劝进文的作者多年后会不会像王垠一样，能够坦诚的承认自己的错位。我也不知道这些 Linux 劝进文的作者多年后会不会像王垠一样，能够坦诚的承认自己的错位。

画龙画虎难画骨，譬如皇帝的新衣。以模仿开始，无论怎么看，都注定了 Linux 败局已定。

> ***Those who do not understand Unix are condemned to reinvent it,poorly.***（那些不懂 Unix 的人注定要重复发明一个蹩脚的 Unix）
>
> ——[Henry Spencer](https://www.nasa.gov/history/alsj/henry.html)

### 01 成也 GPL，败也 GPL

> **为什么 GPL 是更好的开源许可证?**
>
> 作者阮一峰无论是技术性还是非技术性的内容，都是在 ***云***，不具有任何可参考性，写 GPL 的文章一看就是连 GPL [原文](https://www.gnu.org/licenses/gpl-3.0.html)甚至[中文机器翻译](https://jxself.org/translations/gpl-3.zh.shtml)都没看过，典型是在云。全文写 GPL，没有一处引用了 GPL，不觉得荒唐吗？而且理解完全错误（更多请见本文），综合其他技术性文章，基本断定其网站的所有内容都是在云。——[为什么 GPL 是更好的开源许可证?](https://www.ruanyifeng.com/blog/2010/02/why_gpl_is_a_better_choice.html) 很简单，因为你在瞎编，你连 GPL 三个字母怎么翻译都不知道。你写的它压根就不是客观存在的 GPL。

GPL 许可证给人们带来最多的感受绝不是“free”，而是“传染”、“感染”，似乎 GPL 是一场瘟疫，传到哪里都会带来灾难。而且似乎对其误读的人不在少数，GPL 之“free”，不是免费，而是更接近“libre”。对于 GPL 来说也并不意味着你的代码会被 100% 开源下去，得到回馈。著名的例子就是 Boox——一家使用了 GPL 代码却没有开源的 Eink 生态链公司。

FreeBSD 之所以要与 GPL 划清界限是因为 GPL 阻碍了 FreeBSD 的发展目标——One of the ongoing goals for the FreeBSD base system is a migration to modern, copyfree or at least more permissively licensed components. FreeBSD 基础系统的一个持续目标是迁移到现代的、宽松授权条款或至少是更多许可的组件。

如果有人说 BSDL 会被大型公司滥用，那么 Anti-996L 才是最佳许可证，而绝不是什么 GPL。因为任何许可证都会被滥用（除了 Anti-996L ）Anti-996L 才是世界上最好，最优秀的许可证。保证了你的代码不会被任何公司滥用——因为没有公司敢用。

Apple 公司复用了大量的 FreeBSD 代码，同时也为其提供了资金以开发 LLVM，类似的，还有英特尔和 Netflix。

被“利用”不一定是一件坏事。毕竟只有没有任何价值的东西才不会被利用，只有没有任何用处的“hello world”代码才不会被滥用。也就成了庄子所说的“无用之用，是为大用”。

尽管我们看到了许多开发者由于项目被滥用而删库跑路，但是这件事也是双向的。开源代码开发者往他们的代码里塞圣诞节彩蛋，商业公司及“利用”他们的人就要承担这一代价——无论是被开除还是被质问到你这个按钮到底被谁吃掉了。

得益于 GPL，一个 CentOS 倒下去，千千万万个 XXOS 站起来，肉眼可见，从此以后的教程将更加地复杂，更加地不具备普适性。此前写文章抨击 CentOS 的 Si Feng 说过“CentOS: 永远有多远就离它多远”——如果一定要为服务器挑选 Linux 发行版（假设不考虑其他非 Linux 系统例如 FreeBSD）的话，首要的原则就是尽可能远离 CentOS。[《CentOS: 永远有多远就离它多远》](https://feng.si/posts/2019/07/centos-the-last-linux-distro-you-should-ever-consider/)当时还有很多人抨击他说他荒谬，现在看来谁荒谬还真是不一定。现在看看那篇文章下的回复，不知道斯言仍在，斯人何在？我现在也仿照着他，说一句话——“ Linux ：永远有多远就离它多远”

### 02 “ Linux 真的是个好东西吗”

Linux 真的赶上了一个好时候，其实 Linux 最初和 GNU 是没有半毛钱关系的，GNU 计划一直排斥 Linux，他们想要有自己的操作系统或者说内核，他们管他叫做——GNU Hurd。这一项目至今仍在进行中……

Linux 发行版不过是一堆 GNU 工具+包管理器+ Linux 内核所构成的松散的操作系统（一般将前两者合称为“Userland”）每个人各维护各的，就像 Ubuntu 很少回馈上游社区一样，这也反证了 GPL 许可证的确不如 Anti-996L。

GNU Hurd 错位，Linux 占据了所有开发者的计算机，就像破窗效应那样，如果那些窗没修理好，可能将会有破坏者破坏更多的窗户。越来越多的开发者走向了 Linux 而非 GNU Hurd。可以说是“所有的好东西都给了 Linux ”，那么反过来说集开发之大成的 Linux 是个好东西吗？看上去答案是肯定的，其实不然。

硬件上看，Linux 的 GPL 阻碍了硬件兼容性扩大（他们是怎么解决这个问题的呢？），仍然有许多用户认为 Linux 是完全开源的，他们认为——不开源我是怎么编译的呢？那么“ Linux -libre”项目（<https://www.fsfla.org/ikiwiki/selibre/linux-libre/>）所删减的是什么呢？—— Linux , the kernel developed and distributed by Linus Torvalds et al, contains non-Free Software, i.e., software that does not respect your essential freedoms, and it induces you to install additional non-Free Software that it doesn't contain. Even after allegedly moving all firmware to a separate project as of release 4.14, Linux so-called "sources" published by Mr Torvalds still contain non-Free firmware disguised as source code. Linux，由 Linus Torvalds 等人开发和发布的内核，包含非自由软件，即不尊重你的基本自由的软件，它诱使你安装它不包含的，额外的非自由软件。即使据称从 4.14 版开始将所有固件转移到一个单独的项目，Linus 先生发布的 Linux 所谓的“源代码”仍然包含伪装成源代码的非自由固件。

软件上，Linux 的软件包数量的确很多，甚至比 Windows 的软件还要多，这在一定程度上有积极影响，但是其消极影响更甚。有很多的开发者并没有很好的维护他们的项目，因为他们的 GPL 并不起到任何保证作用，开发者也没有任何义务为软件提供任何保证。可见到的是，先有软件，后有用户需求设计（好吧，实际上压根没有这个东西），他们不在意用户是怎么想的，你想往一个 IM 软件里加一个截图功能，因为类似的 Windows IM 软件（比如 QQ，微信）有这个功能，而且这个功能很重要。但是开发者会和你说，你用其他的软件截图然后复制进来就可以了；或者说我们是 GPL，你看得到源码，你自己去改就是了，你不会改那就是你自己的问题了，和我们无关。你可以随便报告 Bug，但是我们可以简单地说“No”。

安全上，OpenBSD 为了改进其安全性移除了 Linux 兼容层以及其常用的软件“sudo”。Linus 此前就抨击 OpenBSD 团队是一群自慰的猴子（OpenBSD crowd is a bunch of masturbating monkeys），认为他们是玩具。至今人们仍不知道那些年 SELinux 和 FBI 的关系（SELinux (Security-Enhanced Linux ) 是由美国国家安全局（NSA）所开发）嗯，没错，这也是一个 GPL 软件，“你觉得有问题你可以自己去看源代码吗！并给我们指出来。”但是更多人不知道的是 Windows 的开源是没有意义的，几十 TB 的源代码，无论他是开源还是不开源对于何种意义来说都是一样的——你既看不懂，也看不完，等于没开源。

### 03 Linux 的商业布局

Linux 的用户或者说在有商业版发行下的，使用所谓“社区版、开源版”的 Linux 用户其实和他们所嘲讽的使用 Insider 的“小白鼠”没有什么本质上的区别。所谓 Linux 的商业布局就是让更多地用户接触到苦难哲学，接触到一个根本不完善不稳定的软件。

Wine 的商业版叫做 Crossover，境内由著名的“苏州思杰马克丁”所代理。Wine 是一款在类 UNIX 操作系统上模拟 Windows 程序的开源软件，使用起来可谓是苦难哲学到了顶峰。Crossover 则不然，他们以开源为测试模板积累了丰富的经验以改进自己的程序。类似的著名操作系统就是 Fedora——RHEL 的社区版，开源版。

这些 GPL 的软件随时都有闭源的风险，但是他们又说了，GPL 允许 Fork，于是出现了很多李逵的副本——李鬼。比如 Mysql 与 MariaDB、Rcoky Linux 之于 CentOS、OpenJDK 与 OracleJDK……那么到底该用哪个呢？你不知道，因为 GPL 软件防止你滥用他。商业公司真的愿意和开源软件共荣共生吗？答案是否定的，他们只是没有更好的选择而已，君不见使用 LLVM 后的苹果公司怎么看待 GCC。认清这个现实的商业公司正越来越多。

Linux 的商业布局就是让用户免费帮自己测试软件，然后赚钱，“回馈”社区继续让用户帮自己免费测试软件，最后用户还会非常感谢这些公司为他们的开源事业做出的贡献。而用户得到的则是一个充斥着苦难哲学的软件，除此以外，别无长物。按照他们的说法，这也叫做“利用”。

### 04 “大独裁者”未必是好事

众所周知，Linux 的内核开发是由 Linus 一人独裁负责的。我们仍未知道何时独裁也成了一件值得称赞的事情了。或者在他们看来只要项目进展顺利，Linus 选好接班人，Linux 内核就可以像中国的秦始皇所畅想的那样——受命于天，既寿永昌。他们把不同意见的人都打成“左派”，给他们扣上帽子，没有人告诉你，那个年代已经过去了吗？

Linux 的社区和他们的开发风格也是一样的，充满了各种巨苣，巨苣们一言以定天下，其他人说了不算。最典型的就是贴吧，如果你想问 Linux 的开发模式是什么，他们的社区是什么——请看百度贴吧：有五六个自诩代表吧友实则毫无贡献的人，在奔走试图合纵连横试图推翻现有吧主；有一个自称贴吧是自己的私有物品，吧主万世万代都得是自己的小丑；还有一个固定的吧宠，但从来都认不清自己的身份，还在说别人哗众取宠；剩下的都是摸鱼躺平的围观群众。

Linux 社区如 Linus 所言，是一个肮脏的泥潭，任何想要和这些人辩论并试图驳倒他们的人都将会被其拉低智商到同一水平，并眼睁睁地看着他用丰富的经验打败你。

Linux 本人所骂走的开发者绝不在少数，他们的行为准则（CoC）制定了和没有制定是一样的，你是能开除 Linus 不让他贡献一行代码，还是你能让他只做事不说话？类似的 GNU 离开了 Richard Matthew Stallman 会怎样？就像现在这样吗？

### 05 Linux 不会再年青了

我们都知道，引用任何名人名言并不会为自己的论述增加一丝一毫的正确性。

前文所说到的 GNU Hurd 的确在设计上是一个非常优秀的微内核操作系统。但因为错失良机，使得更多开发者投入了 Linux 的泥潭之中。

Linux 被无数人包装成 GNU 计划的伟大产物，GPL 的伟大产物，Linus 独裁领导下的伟大产物。没有任何人可以以任何理由批评他，除了 Linus 本人。事实上这就是皇帝的新衣，你想掀开 Linux 光鲜亮丽的外衣去一窥内部却发现 Linux 外边根本没有穿着任何衣物。

在抨击 FreeBSD 社区以前，请看看泥潭般的 Linux 社区，这不是五十步笑百步，而是大哥莫说二弟。此处的读者可以移步之前的文章——《Linux 社区已经成为了一个肮脏的泥潭》。Linux 社区的那些巨苣，那些搞苦难哲学的是最没有资格说别人的社区肮脏污秽不堪的人——他们天天说着 RTFM。关于 Linux 社区的种种一直无人敢说，无人敢言，任由他们这群巨苣去践踏，去污蔑，去破坏别的社区。

Linux 社区早就不像当年那样了——我们都知道新人的确很菜，也喜欢抱怨，并且带有浓厚的 Windows 习惯，但既然在这里询问，我们就应该有责任帮助他们解决问题，而不是直接泼冷水、简单的否定或发表对解决问题没有任何帮助的帖子。乐于分享，以人为本，这正是 Ubuntu 的精神所在。

他们会把那些问题叫做“日经”，然后将你移出他们的社区。当然你不得不承认有些人是不听劝的：你和他说四遍，发了各种形式的教程（既有图片又有视频还有文字），他说自己照着文档做了，你一看让他发照片。“这就是你做了的结果？配置文件一个字都没有改”他改了后正常运行了，也不会和你说一声谢谢，然后继续问一些“日经”问题，你再回他，他就会说你“指手画脚”，不会指导人只知道让他看文档，妨碍别人教他，然后还去 Linux 社区发帖说 FreeBSD 社区有问题，真是恶人先告状。但是他们往往会报团取暖，觉得对方说的都对，是别人有问题，自己 100% 正确。然后弹冠相庆，互称兄弟。

你告诉他“lib32”兼容层很重要，后边安不上去，必须现在选。他会告诉你“老子就是不用垃圾的 32 位，老子就是要用纯净的 64 位系统，按不上是老子自己的事，你管不着”，“既然你都懂那还来问些什么呢？”。这种人是没有任何资格抱怨 FreeBSD 社区的，他们连最低水平的素质都没有，他们只配在泥潭般的 Linux 社区待着，是 Linux 社区造成了他们这种畸形的人格的变态的心理——无论是提问者还是回答者，谁也看不上谁。

与 Linux 相关的荒谬事件更是数不胜数。一个 systemd 与 SysV init 的争论就搅得 Linux 界七荤八素。Systemd 试图统管一切——网络，日志，磁盘管理，引导，时钟，电源、Cron、区域语言……然后就造成了各大发行版的分裂，虽然已经很分裂了。更别说前文提及的 SELinux 这种东西是怎么进入 Linux 内核的了。红帽公司——他们引以为豪的 Linux 的商业布局正在一步一步地控制整个 Linux 的发展。Linux 的工具属性越来越强，那个曾经年青有趣的玩具般的 Linux 早已不在了。

### 06 屠龙者终成恶龙

Wer mit Ungeheuern kämpft, mag zusehn, dass er nicht dabei zum Ungeheuer wird. Und wenn du lange in einen Abgrund blickst, blickt der Abgrund auch in dich hinein. 与恶龙缠斗过久，自身也会成为恶龙；当你凝视深渊，深渊也在凝视你。

——Friedrich Wilhelm Nietzsche

Linux 打败了一系列的操作系统：GNU Hurd、FreeBSD、OpenBSD 以及其他一堆 BSD，在服务器领域击败了 Windows server、MacOS，在移动平台产生了 Android。

Linux 的发展看上去是 GPL 的胜利，是 Linus 独裁的胜利，也是这个开源社区的胜利，更是 Linux 商业布局的胜利。

事实果真如此吗？究竟是皇帝的新衣还是破窗理论呢？

新事物必将取代旧事物，万事万物的新陈代谢如此，Linux 也不会永远长久下去，终究有一天会有更优秀的操作系统脱胎于此，并取代他。这是事物运行发展的基本规律，无可避免，而这些人所做的只是为 Linux 延长寿命而已。看上去蓬勃发展的 Linux，其实早就垂垂老矣。

Linux 败局已定。

只是没人愿意揭开这皇帝的新衣罢了。

屠龙者终成恶龙—— Linux 和 GPL 正在阻碍着越来越多的新技术发展。他们逼迫人们耗费着大量的人力物力去维护一堆堪称“屎山”的代码——每错，我说的就是你们：GCC、Xorg 以及其所谓的替代品 Wayland。

### 07 结语

Linux 已经日薄西山了，尽早投入 GNU Hurd 的怀抱才是真正明智的选择，尽早离开 GPL 选择 Anti-996L 才是真正自由的选择。

当然，不管 Linux 是不是皇帝的新衣，有多么的苦难哲学，他都给这个世界带来了一种选择，时势造英雄，Linux 乘势而来，也必将乘势而终。

Linux 内核的版本号已经刷到了 5.17-rc5，那么也许还会有 6.17-rc5、7.17-rc5、8.17-rc5……

但是 Linux 败局已定，且无人能够拯救他。我们能做只是尽量去多使用他做一些事情，最后发挥一下 Linux 的余热。

## FreeBSD 败局

> [还有人记得 Linux 之前，那个理想又骄傲的 BSD 吗？](https://my.oschina.net/u/5324949/blog/5434988)
>
> 作者：lola
>
> [FreeBSD 大败局](https://my.oschina.net/oscpyaqxylk/blog/5457229)
>
> 作者：肖滢 & lola

首先不知道何为 FreeBSD 大败局的建议阅读下以上 2 篇文章，当然当初我很快给出了我粗浅的回应：

[Linux 败局已定——驳 FreeBSD 大败局](https://book.bsdcn.org/di-19-zhang-wen-xue-gu-shi/di-19.7-jie-xiao-shuo-freebsd-cong-ru-men-dao-pao-lu.html)

文不加点，当时写得很快，不到两个小时就写完了，而且并没有动什么脑子。可能就是意气用事，为了反驳而反驳吧。当然我也没打算说他在现在就是正确的了。我只是觉得现在更加值得花时间来在文档和代码之外来谈论一下这些更加吸引人的东西。

> 看过上一篇文章《还有人记得 Linux 之前，那个理想又骄傲的 BSD 吗？》的读者都知道， BSD 是 Unix 最重要的一个开源分支，这一本该坐上 “开源头把交椅” 的操作系统家族承受了一场足以记载史册的浩劫。
>
> 时间倒回三十年前。1993 年，那时候 BSD 正处于水深火热，Linux 刚诞生没多久，[Meta 杂志](https://gondwanaland.com/meta/history/interview.html) 问 Linus Torvalds：能不能推测一下 Linux 在市场上对 Unix 的影响？当时，Linus 的回答是：
>
> > I have gotten various mails and seen some newsgroup messages about persons who have switched over already or would like to switch over once Linux is able to run commercial binaries, but at least so far, I doubt Linux has dented the real Unix market very much.
> >
> > 尽管我已经看到一些人已经或者想要切换到 Linux，用于运行商业二进制文件。但目前为止，我不认为 Linux 已经严重削弱了 Unix 的市场。
>
> 彼时，Linux 初出茅庐，尽管锋芒毕露，但谁也不知道以后到底会发生什么。须臾三十年，形势调转，Linux 现在的地位有目共睹。
>
> 另一边，BSD “灾后重建” 且大受欢迎的 386BSD 因为内部意见不同出现问题，其中三个补丁包协调员 Nate Williams、Rod Grimes 和 Jordan Hubbard 另起炉灶，于 1993 年创建了 FreeBSD。尽管还有 NetBSD 和 OpenBSD，但后来的事实证明，FreeBSD 发展最好、走得最远，是 BSD 世界里的 “扛把子”。

> 在之后的日子里，FreeBSD 没能重现 BSD 的往日荣光，反而一直生活在 Linux 的阴影之下。**“Linuxism”** 成为 FreeBSD 内部常常挂在嘴边的一个词，其中透露出酸酸的比较之味。
>
> 一方面，FreeBSD 坚定地沿袭 Unix 的一些传统，坚决地想要与 GNU/Linux 保持距离；另一方面，FreeBSD 也在积极地寻求更长足的发展，想要至少在某些方面保持优势。
>
> 世事如棋局，得势者得天下。以势定夺，怎么看 FreeBSD 领到的剧本都是一个 **“大败局”。**

Linuxism（Linux 主义/歧视）真的只是一种 FreeBSD 吃不到葡萄就说葡萄酸的牢骚话吗？光阴荏苒，时光如梭，自由软件运动持续了半个世纪有余，能够留存至今并真正意义上具有使用价值和能力的操作系统寥寥无几，更遑论开源操作系统了。自由软件运动所推崇的操作系统或者说内核（实际上是微内核） GNU Hurd，反正我是没用过……

如果你使用了 systemd 还实现了所有的 Linux ABI，并且用了一大堆的 GNU 软件，而且你的内核也实现了所有的 Linux 特性，只有包管理器不一样，那么你究竟是 Linux 呢还是你自己的操作系统呢？这看上去是一个忒休斯问题。实则并不难回答。

而今几乎所有的 GPL 软件都使用 Linux 作为自己的开发测试平台，并且结合了越来越多的 Linux 特性，乃至于让 Eclipse IDE 这种 java 软件都失去了可移植性。他们只会说你的系统我们并不关心，你自己打补丁就是了，因为我们只用 Linux。他们与 Linux 内核的某个特性紧密结合，并且死死捆绑。仿佛这些软件不依赖 systemd 就活不下去一样，比如 todesk——他们认为“（todesk）没必要兼容 init，反正我用的 systemd，谁还在用那玩意”，他们官方 Linux 版本 QQ 群里的管理员就是这么说的。

FreeBSD 恪守古老的 UNIX 法则，坚持其 BSD 开源哲学，坚持基本系统去 GNU 化。这意味着你不会遇到用包管理器就卸载了所有内核或者 glibc（C 库）这种蠢事。基本系统的软件都由 FreeBSD 项目统一维护，Linux 则没有基本系统这个概念，或者说 Linux 系统就是由一个个软件包拼凑起来的，如果你用过 LFS/Gentoo/ArchLinux 就会有明确的体验。一切命令/二进制文件都是由软件包或者 shell 提供的，也就都可以用包管理器来管理，比如说卸载……所以不难理解包管理器卸载内核这件荒唐事。

FreeBSD [去 GNU 化](https://wiki.freebsd.org/GPLinBase)是贯彻其 BSD 哲学的实践。FreeBSD 项目认为基本系统中的 GNU 软件（很多常见的比如 grub vim nano tar 等）都会阻碍人们对 FreeBSD 的充分利用，因为人们被迫接受了 GPL 这一强制性开源的协议，不利于其更加自由的使用。这是出于 BSD 与 GPL 观念上的不同——GPL 强制开源（虽然也有很多方法隔离污染，比如 Android 所做的），而 BSD 则允许闭源（比如 Chromium）但是这并不意味着 BSD 强制性的要求用户不能使用 GNU 软件，它只是基本系统（你安装好的系统）中去 GNU 化。你完全可以自己替换（实际上也不难，用包管理器一个个安上就是了），毕竟 FreeBSD 完全是自由的。

事实上，**并非是 FreeBSD 在去 GNU 化，而是 Linux 本身在 GNU 化，** 同时这也阻碍了 FreeBSD 的现有技术优势的组件无法进入 Linux 内核，比如 ZFS。

但是我看不出 FreeBSD 能有何出处了，这也是现实——引以为豪的 TCP/IP 远远落后于 Linux，BBR 移植了数年仍然性能低下；驱动问题更是难以解决，甚至放弃了对自己的英特尔驱动的维护，转而使用了 linux drm；zfs 更是已经被引入了使用人数最多的 Ubuntu，不再是 FreeBSD 等少数系统的专属了。

或许 FreeBSD 真是一个败局吧？

> 01 成也 BSDL，败也 BSDL
>
> > 正是我们的许可证，使得我们独一无二。与 GPL 尤其是 GPLv3 相比，BSDL（BSD 许可证）对很多厂商来说是非常重要的。
>
> 2021 年 3 月，FreeBSD 13.0 版本最新发布。在一场[采访](https://www.theregister.com/2021/03/10/the_state_of_freebsd)中，FreeBSD 内核开发者 John Baldwin 如是说。
>
> 他说得没错。许可证是 BSD 一族与 GNU/Linux 最显著的不同，它彰显了 FreeBSD 所继承的、与 RMS 提倡的 **“Free”** 完全不同的 **“Libre”** 哲学态度，使得以 FreeBSD 为代表的这些开源软件自成一派。
>
> 在 GNU 理念里，软件本该自由，专有软件不应该存在。因此，GPL 被设计得具有传染性，并且要求所有修改后的代码都要返回上游，当初 Linus 选择 GPL 正是看重后面这一点。而 BSDL 则更接近于 **“公共领域”**（公共领域的作品属于公有文化遗产，任何人可以不受限制地使用和加工它们），几乎给了使用者最大权限的自由，不但可以自由地使用、修改源代码，不需要返回任何修改，还可以将修改后的代码作为开源或者专有软件再发布。
>
> > 我们并不认可 GPL，它是一种政治宣言。我们想要将我们的许可证与政治分开。 GPL 会吓跑很多潜在用户，这只会适得其反。
> >
> > —— FreeBSD 创建者之一 Jordan Hubbard
>
> 因此，在之后的实践中 FreeBSD 也在竭力与 GPL 划清界限。多年来，FreeBSD 一直致力于删除基础设施中的 GPL 软件，以便 “迁移到现代的、CopyFree 以及许可更宽松的组件”。比如：用 LLVM 的 LLDB 替代 GDB 调试器、使用 BSDgrep 替代 GNUgrep，以及[删除](https://www.oschina.net/news/126887/freebsd-q4-2020-report) libgnuregex 等等。（其中，FreeBSD 为了完成向 LLVM 的迁移，花费了十年左右的时间，因为 [LLVM](https://www.oschina.net/news/170236/llvm-relicensing-update-2021) 是在 Apache 2.0 下获得许可，限制比 GPL 更少。）
>
> FreeBSD 的这种身份主张无可厚非，但从现实层面来考量这两个许可证，就是另一码事了。
>
> 阮一峰老师在[《为什么 GPL 是更好的开源许可证？》](http://www.ruanyifeng.com/blog/2010/02/why_gpl_is_a_better_choice.html)一文中作了逻辑阐述：
>
> > 当程序员放弃代码的版权，或者选择 BSD 许可证，他可能认为自己做出了世界上最无私的行为。很大程度上，事实确实如此。但是，我们要知道，**这个世界是一个商业利益占主导的世界**。一旦发生像甲骨文拥有 MySQL 这一类的事情，你的代码的价值将大大削弱，大公司先是免费利用它们，然后再设法推出取代它们的私有产品。你以为自己奉献了爱心，但是实质上变成了为大公司无偿打工。
>
> > 从这个角度看，**GPL 是更好的开源许可证**。它保证了自由始终是自由，既无法被剥夺，也不是一种圈套或陷阱。

实际上，该博客的这篇文章是有一些问题存在的。

作者阮一峰指出：

> 即使 mysql 闭源一定会有其他人接手，继续推出 MySQL 的后续版本…但是只要代码完全兼容…

如果闭源了并推出新产品，那么如何还能做到代码完全兼容？就拿如今红帽 RHEL 的代码授权来说，红帽把开源的代码水平降级到了 CentOS stream，你即使有 rockylinux、欧拉、阿里龙蜥等一堆系统，你的兼容级别也是次于 RHEL 的。

> 第二种情况：甲骨文公司决定，MySQL 的后续版本不再开源，或者整体并入 Oracle 数据库，会怎么样？
>
> 答案更简单，不可能发生这种情况。因为根据 GPL 许可证，只要发布基于原代码的新产品，就一定必须开源。

GPL 不是用来限制作者或者版权方自己的，否则按照这个逻辑，没必要 fork 出来 MariaDB。版权持有者完全可以决定后续版本的开源与否。

> > 严格来说，GPL 是由开发者对其他人发布的的许可证，用于这些人使用、发布和改变该程序。开发者本人并不受到许可证的限制，所以无论开发者做什么，这都不是“违反”GPL。见 <https://www.gnu.org/licenses/gpl-faq.html#DeveloperViolate>

> 让我们再来假想一下，如果 MySQL 的源码处于公共领域，或者 BSD 许可证之下，那会怎样？
>
> 那样的话，许多站长恐怕都会感到大难临头了。他们不得不做出选择，将来到底是升级到第三方小公司推出的、质量没有保证、支持力量薄弱、互相不兼容的基于 MySQL 5.x 版本的各种衍生数据库，还是升级到甲骨文公司推出的、与 Oracle 兼容的、号称具备各种新功能和最佳性能、并且广告满天飞的 MySQL 6.0 版本。

在类似 BSD 许可与 MIT 许可的 PostgreSQL 许可下发行的 PostgreSQL 为什么没有发生作者博客所提到的问题呢？反而实用性更超 MySQL。

> GPL 是更好的开源许可证。它保证了自由始终是自由，既无法被剥夺，也不是一种圈套或陷阱。

那么问题来了，GPL 究竟保障的是人们的消极自由还是积极自由呢？见仁见智。此外，绕过 GPL 的事情以及技术手段不在少数。作者阮一峰博客底下评论的 Android 就是一例。而且根据已逝 VIM 作者 Bram Moolenaar 的话“它（GPL）事实上是通过限制自由来实行自由的”，也即 GPL 是一种“伪式开源”，并非真实的开源。

> FreeBSD 的贡献者就常常被调侃为 Apple 公司的无薪员工。Apple 将社区工作都纳入了 FreeBSD，在其基础上进行了一些更改，就变成了一个专有的、非自由的操作系统。
>
> 糟糕的是，Apple 还对内核和其他部分进行了分叉，并将其命名为 Darwin，这一系统基本就远离了 FreeBSD 的传统。而且，由于 Apple 支付了版税，他们可以合法地将其称为 Unix，但这笔钱也没有流向 FreeBSD。

实际上有不少 Apple 开发者同时是 BSD 开发者。Apple 也是 FreeBSD 基金会的赞助商之一。

> 更过分的是，相较于 Netflix 等，同样是 FreeBSD 受益者，Apple 为上游做贡献的积极性也不足（因为 BSDL，贡献上游这事就全凭自觉了）但 FreeBSD 的人对此倒也看得开：“我不会因此而责怪他们。FreeBSD 是一个 BSD 许可的项目，而不是 GPL。”John Baldwin [表示](https://www.theregister.com/2021/03/10/the_state_of_freebsd)
>
> > BSD 许可证就是一个复制中心，可以为所欲为，但我们不在乎。
>
> —— Marshall Kirk McKusick ，他亲身参与了 4.3BSD 和 4.4BSD 的开发和发行，后来又深度参与了 FreeBSD
>
> 因为 GPL，这种事永远不会发生在 Linux 身上。在 GPL 许可下，任何人都可以使用 Linux，但是有一个强制要求，如果修改后的版本要出售或者提供给他人，则必须根据相同的 GPL 许可把完整源代码对外发布。如此一来，**GPL 可以确保 Linux 永远不会成为专有产品，所有开发者做出的贡献最终会回到社区，Linux 可以得到更好的发展。**

实际上并非如此，比如 Ubuntu 很多情况下都在重复造轮子。Linux Kernel TTY 中文补丁一直不被接受。开发者只会按照自己的意图改造软件，面对用户的需求往往充耳不闻。Linux 是不是会成为专有软件我不知道，但是我知道他离改名叫 Systemd OS 那一天不远了。也早已经放弃了自己以往的 UNIX 哲学。

> 四、转发完整副本
> 　　你可以免费或收费转发，也可以选择提供技术支持或品质担保以换取收入。 <https://jxself.org/translations/gpl-3.zh.shtml>

因此根据 GPLv3，[红帽的做法](https://www.redhat.com/en/blog/furthering-evolution-centos-stream)似乎是无可指责的。

另外关于开源，源代码是可以以售出方式开源的。

Linux Kernel 的开发相当地封闭，你如果有内核补丁要提交必须挨个按照脚本上给出的邮件地址去询问，看看谁愿意接受你的补丁。而 FreeBSD 则是真正任何人都可以参与开发。

> 在 Linus 眼里，GPL 就是他想要的，而不是 BSDL。
>
> 许可证是 Linux 成功的决定性因素之一，因为它强制你必须回馈。如果你真的想创造更大的东西，如果你想围绕它创建一个社区，BSD 许可证不一定是很好的许可证。它（BSDL）会让开发人员觉得大公司在利用他们的工作。

BSD 认为开源的最大目的并非是出于所谓自由，而是让代码尽可能地被复用，以产生尽可能大的社会效用。而不受任何限制。

> 02 “好东西都给 Linux 了”
> Linux 赶上了好时候。
>
> Internet 开始风行之际，Linux 的开发者及爱好者正好能透过 Internet 实时地发布新闻、想法、提问、讨论、递送程序代码及进行错误回报。这种由 Internet 连接起来的分布式合作方式带给了 Linux 惊人的活力。**这种生命力直接将 Linux 送上了可以与 BSD 分庭抗礼的位置。**
>
> 与此同时，在 Linux 现身之时，刚好是人们开始买得起个人计算机时。那是还没从诉讼中缓过劲的 BSD 对于当时的个人计算机所使用的 80386 硬件的支持度非常不好，Linux 几乎成为当时大众的第一选择。**这一波路人缘，Linux 收割得很漂亮。**
>
> BSD 缺位，Linux 趁机发展，刚从灰烬里重生的 FreeBSD 碰上的局面就很残酷：**Linux 占据主导地位之后，已经形成马太效应，之后的态势呈现出强者愈强、弱者愈弱的趋势。**

我到更觉得是一种破窗效应。现在 Linux Kernel 里面塞进了太多的垃圾。代码看起来也是糟糕一团。甚至还有不少人[拿他刷起来了 KPI](https://lkml.org/lkml/2021/6/18/153)，以及各种“社会学”[投毒实验](https://lore.kernel.org/linux-nfs/YH%2FfM%2FTsbmcZzwnX@kroah.com/)

> **硬件方面**，Linux 可以在许多不同的平台上运行，而 FreeBSD 则不行。硬件设备制造商更愿意为 Windows、Linux 等主流的操作系统提供驱动程序，IBM、戴尔和惠普直接支持在其服务器上运行 Linux，但处于主流之外的 FreeBSD 可能不在它们的考虑范围内。

FreeBSD 支持的架构难道很少吗？那不如试试 NetBSD 吧。

> 此外，Linux 的开发者数量比 FreeBSD 多出数倍，这意味着 Linux 拥有更多的贡献者和测试新硬件的机会。长期下来，最终导致 FreeBSD 的兼容性和硬件支持远远不如 Linux。比如，用户需要定期更新图形驱动程序，Linux 可以更早、更快地提供支持。
>
> 软件上，Linux 软件包存储库的数量远超过 FreeBSD ，具有更大的灵活性和可用性，虽然 FreeBSD 也提供了预编译的软件包，但它仍然无法与 Linux 可用的资源进行比较。其实，这都是互为因果关系的 —— 因为 FreeBSD 市占率比 Linux 低多了，开发者少，很多软件对其的支持度就不如 Linux，这又反过来加剧了其市占率的下降 —— 一个 **死循环**。

FreeBSD 有 Linux 兼容层，所以理论上软件数量应该远超 Linux。另外上边已经讨论过，专属依赖于 Linux 的软件越来越多，这并非一件好事，这会导致所有软件丧失独立性和可移植性，出现共同的故障点。自由软件运动如果再这么进行下去，那想必所谓“开源”开不开已经没有多大意义了，因为离开了 Linux 或者 Systemd 软件根本跑不起来，也无法移植。

> 有人评论很是贴切：“所有的好东西都给了 Linux”。
>
> 看着 FreeBSD 如今的现状，用户都着急了。2020 年 3 月，一些用户开始在推特上催促 FreeBSD 基金会尽快赞助 FreeBSD，以推进对 802.11ac 支持的开发工作。要知道这个时候， Windows 和 Linux 都提供了对 802.11ac（"WiFi 5"）的良好支持，并且已经开始将重心放在 802.11ax （"WiFi 6"）上了。

> 03 FreeBSD 没有布局
> Linux 内核是个操作系统 “半成品”，企业支持的重要性不言而喻。支持 Linux 的著名企业有 RedHat 、SUSE、IBM 、Canonical 等等，它们不仅贡献了许多实用性很强的发行版，如 Fedora、Ubuntu、Arch Linux、Debian、Linux Mint 等，同时确保操作系统实现快速更新。
>
> 有人认为， **RedHat 是 Linux 快速进入商用市场的关键性因素之一**。因为对于大型企业而言，或许授权费用的多寡并不是重点，他们要的是能够说服上司及股东的解决方案。透过 RedHat 所提供的技术支持，信息部门有了底气将 Linux 列入解决方案之中。
>
> 这项优势几乎是 FreeBSD 所难以匹敌的，因为 FreeBSD 几乎没有商业支持。

如今看来似乎并非如此？红帽的商业布局如今让开源界啼笑不止。Linux 的确是快速进入商用市场了，但是给开源界带来了什么呢？红帽的商业布局就是为了使 Linux 世界变成 systemd 世界。红帽及大型公司已经在事实上把控了 Linux 的开发的上下游。

> 因为缺乏商业公司运作的商业版本，为 FreeBSD 提供支持的企业屈指可数，没有大量企业为终端用户提供大规模的技术和服务支持。
>
> 在 FreeBSD 13 发行之后的那场采访中，当被问及商业模式问题时，John Baldwin 这样回答：
>
> > 有很多来自像 Netflix 这样的公司，内部会有 FreeBSD 专家团队开发功能，这些工作直接进入上游 FreeBSD。还有一些资源来自学术和业余爱好者。最近越来越多的工作由 FreeBSD 基金会承担，基金会接受捐赠资助。
>
> 可以看出，一些接受了 FreeBSD 恩惠的企业的确在以某种方式去推动 FreeBSD 的生态发展，但与 Linux 所得到的商业支持，完全不能相提并论。
>
> 就像有人说得那样：“尽管 Netflix、Apple 和 Juniper Networks 等公司都在支持 FreeBSD，但它们并没有像 Canonical 和 RedHat 等公司那样投资它，**共荣共生的传奇只发生在了 Linux 上** 。”

> 04 “大独裁者” 未必是坏事
>
> > One of the major problems with 386BSD seems to be the lack of co-ordination: that may sound weird coming from the Linux background, but in fact the 386BSD project seems to suffer from a lot of people working on the same thing due to the long release cycle.
>
> > The NetBSD project may be a step in the right direction, but I think 386BSD has been hurt by the way it has been developed.
>
> > 386BSD 的主要问题之一似乎是 **缺乏协调管理**：尽管我以 Linux 的角度和身份来看很奇怪，但事实就是这样，因为较长的发布周期，386BSD 里大量的人都在做同一件事情。
> >
> > NetBSD 可能走对了方向，但是 386BSD 已经因为这种开发方式受到了伤害。
> >
> > 1993 年，Linus 一语成谶。很快，386BSD 分裂成为 FreeBSD 和 NetBSD。

> 当时有人总结到：“BSD 走的是教堂式的学院派路线，而 Linux 则是代表了市集式的骇客精神。” Linus 是著名的独裁，而 BSD 对 “独裁者模式” 的嗤之以鼻是一以贯之的。

> 有一个古老的笑话是这样的：如果你把 10 个 BSD 开发人员锁在一个房间里，当你打开门时，你会发现比萨饼不见了，BSD 开发人员死了，还有 11 个 BSD 的新变种。

这句话如今形容 Linux 颇为恰当。

> > 虽然有点自负，但我认为只要我愿意充当傀儡，我本可以阻止社区分裂。当时我在那个位置上已经 10 多年了，我觉得是时候将衣钵传给他人了。老实说，我没想到会这样（指分裂），我以为会出现很多不同发行版而已。
>
> McKusick 曾这样表示。在他看来，Linux 的独裁者模式一样不可取，一旦 Linus Torvalds 离开，就会酿成灾难，Linus 在试图创造超越他自身的一些东西，而 “如果我被公共汽车撞了， BSD 不会真正受到太大影响。”
>
> 这样左派又带点傲气的观点，真是典型的 BSD 的啊。而 FreeBSD 之后出现的管理和开发方式问题，多多少少也带了一些遗传在身上。
>
> 从开发过程上看，FreeBSD 与 Linux 最大的不同就是 —— **没有一个大独裁者**。
>
> FreeBSD 有一个核心团队，相当于公司里的董事会，他们通过授予、撤销修改、提交新代码到代码库等权利来控制访问，其首要任务是确保整个项目处于良好状态并朝着正确的方向前进，并每 2 年选举一次。
>
> “我们主要用邮件列表进行协作，这与 Linux 内核邮件列表相同。但是，FreeBSD 基础系统是一个单一的存储库，内核、C 库以及工具链，所有基础系统实用程序，如 ls 和 shell，都在一个单一的存储库中，一起构建和发布。” FreeBSD 基金会项目开发总监 Ed Maste 在 2021 年表示。
>
> 这种 “核心小组” 型的模式最大的缺点就是很难达成共识，从而延误时机。FreeBSD 核心团队成员 Benno Rice 就曾探讨过这个问题：
>
> > 开发项目的源代码是其核心资产，必须妥善保管。所以项目需要一个源代码管理系统。最初，FreeBSD 使用 CVS，这在当时是一个合理的选择，但直到 2008 年 FreeBSD 还在使用 CVS。为什么呢？因为大家对于应该用什么来代替它没有达成共识。考虑过 BitKeeper、Git 和 Mercurial，最后都无疾而终了。
>
> > 很多社区都会反复出现长期的争论，FreeBSD 也不例外。2008 年，经过八年的争论，Peter Wemm 强行推进了向 Subversion 的转换；从那以后，抱怨声相对较少了。
>
> > 相比之下，Python 从 CVS 开始，2004 年转移到 Subversion，2009 年转移到 Mercurial，现在又转移到 GitHub。在 Python 社区中，一旦 PEP 获得批准，就可以继续进行了，而 FreeBSD 没有这样的机制。
>
> 而 Python 社区，又是另一个以独裁者领导而著称的项目。
>
> 其实，“核心小组” 模式并非只有 FreeBSD 一家，GNU 项目 、Apache Web 等也都采用这种模式。但很明显，FreeBSD 的这个核心团队，并没有做好这份工作。

这里我要提一下，我也持相同观点，FreeBSD 不仅仅是核心团队，其有权限的 committer 也都没有做好自己的工作。他们的观点是大家都是志愿者，因此没有任何可指责的地方。但是我实在是很难认同闭门造车，做任何大的改动都不会在邮件列表讨论一下乃至提一句说我要这么干了。

比如把默认 root shell 从 csh 切换到 sh，我竟然一年后多才知道这件事。这意味着所有的 handbook 教程以及我们社区的教程都需要重新编写以兼容他的操作。这是一件很小的改动，只涉及了几个字母，但是对于下游或者用户来说，是灾难性的。

这种事情，绝不少见：FreeBSD 的安全公告使用了在文件夹名 Windows 下无法支持的冒号“：”，这导致的后果也是灾难性的，你甚至都无法 git 下来项目以参与贡献。但是这种严重的 Bug 似乎并不能引起他们太多的重视。

> 比如著名的 “ Matthew Dillon 事件”（下文会详细说），他们不但没有及时引进相应的行为准则来规范大家的行为，更是对开发者互相掐架、成员参与 “Gamergate” 在线骚扰活动等恶劣行为无能为力。又比如，因为缺少保证质量代码的审查流程，他们还差点让 4 万行有缺陷的代码[混入](https://arstechnica.com/gadgets/2021/03/buffer-overruns-license-violations-and-bad-code-freebsd-13s-close-call/) FreeBSD 内核里。

> 05 “FreeBSD 不会再年轻了”
> LWN 是这么评价 FreeBSD 的：
>
> > 这是一个伟大的项目，但它确实存在一些问题，特别是三点：FreeBSD 很大，它很旧，而且它行动迟缓。FreeBSD 不会变得更年轻了，它难以改变 **一些根深蒂固的态度**。
>
> 的确，从 1993 年 11 月开始，FreeBSD 出生就自带故事，而且它基于的代码非常古老。Benno Rice 说，直到 2017 年 FreeBSD 开发人员才发现自动化测试，而要进行自动化测试，软件必须具有正确的结构，但 FreeBSD 这个 “老家伙” 并不具备。因此，当他在一场活动中看到 Rust 社区有关自动化的演讲时，他就在想：为什么 FreeBSD 不能有这么好的东西？
>
> 不光是古老，FreeBSD 还失去了活力。
>
> FreeBSD 联合创始人 Jordan Hubbard 曾经是社区最为活跃的核心人物之一，2001 年他离开了 FreeBSD 社区，去了 Apple 公司，帮 Apple 捣鼓 Darwin。在他的[辞职信](https://web.archive.org/web/20020615105041/http://kerneltrap.org/node.php?id=169)中，他这么说：
>
> > Another reason, and I hate to say this but it probably needs saying, is that being in core is honestly not what it once was. For a old-timer like myself, who was used to a core team that was far more cohesive and generally on the same page, it's simply a painful experience a lot of the time.
> >
> > Perhaps this is due to overly rose-colored recollections of the old core on my part, and I do certainly recall us having more than our share of disagreement and inefficiency in the past, but on the balance core still feels too much like the pre-WWII Polish Parliment sometimes, where we're fully capable of arguing some issue right up to the point where tanks are rolling through the front door and rendering the whole debate somewhat moot.
> >
> > 还有一些原因，我本不想但不得不说，老实说核心团队已经不像从前了。作为一个老前辈，我习惯了那样的核心团队：更加团结且大家都是一条心，一起经历了许多艰难的日子。
> >
> > 或许是我对旧时光的滤镜太重了，在回忆里我们过去的确有更多的分歧和低效，我们的核心团队实在太 “反应迟钝” 了（这里用了一个典故，二战时德国都已进入波兰，而波兰国会还在商讨对策）我们完全有能力解决问题，但就是这样：坦克都已经在门前了，一切辩论都毫无意义了。
> >
> > Jordan Hubbard
>
> 在这副古老的身躯上，当我们掀开 FreeBSD 那袭表面华丽的裘衣，又会赫然发现上面还爬有一些不那么体面的虱子和臭虫。在圈子里，总是会有一些有关 FreeBSD 的 “小差评”：
>
> > FreeBSD 是一个很棒的操作系统，但 FreeBSD 论坛是我见过的最刻薄的论坛之一。有人在里面寻求帮助却被贬低，并让其滚回到 Linux 社区。
>
> > FreeBSD 论坛成员都是 FreeBSD 的狂热分子，当话题涉及到在 FreeBSD 作用不大的组件时，就会被攻击为 “Linuxism”。
>
> > BSD 论坛一点也不友好。不要在那里问，他们只会让你去阅读手册。你只能靠自己。
>
> > 在 FreeBSD 论坛寻求帮助，得到的回复往往都是：一定是你做错了，因为 FreeBSD 永远不会错。
>
> 当然，人无完人，每个社区都会有这样那样的差评，这些差评或许并不能说明些什么，但是当一些群体性事件爆发出来，FreeBSD 在 **文化和风气** 上的短板就暴露无疑了。
>
> 其中最著名的就是前文曾提及的 “Matthew Dillon 事件”。Matthew Dillon 是 1994 年就加入 FreeBSD 的明星成员。之所以说他是明星，是因为这哥们确实实力过硬，但不合适团队合作，不怎么在乎别人的辛苦成果，是个 “Rock-star” 式的人物。
>
> 当初还在更新 FreeBSD 5 （现在都已经 13 了）的时候，Dillon 想打破 FreeBSD 里一个很大的内核锁，John Baldwin 也想过，于是俩人就一起干了。不出意料，两人在关键部分出现了分歧，Dillon 一意孤行地提交了更改。这引发了非常激烈的争论，在长达一个月的争吵之后，Dillon 退步了，核心团队取消了他的提交权限，他最终也离开了 FreeBSD。
>
> 这不是 FreeBSD 里的孤例，还有很多类似的事件发生过。而这件事直接引起了 FreeBSD 核心团队的反思：**如果 FreeBSD 当时有既定的行为准则，会不会得到更好地处理呢？**
>
> **Dillon 走后，Gamergate 事件直接促成了 FreeBSD 的行动**。简单来说，Gamergate 是一个与性别政治有关的运动，最开始是一个已经离开的 FreeBSD 成员写了一个 Perl 脚本来阻止 Gamergate 参与者的活动，并惹怒了那批人，使得 FreeBSD 惹火上身；再后来又有 FreeBSD 成员加入 Gamergate 并开始在 Twitter 上攻击那个前成员，这下完全把 FreeBSD 拖下了水。
>
> 这一事件不仅引起了激烈的讨论，攻击者随后还将对话日志泄露给了 Breitbart，核心团队别无选择，只能参与进来。
>
> 2018 年， FreeBSD 确立了社区行为准则（Code of Conduct，CoC），这一准则从 LLVM 衍生而来，要求社区开发者友好耐心、热情好客、体贴、相互尊敬、对他人友善、注意不要乱说话、持不同见解时多换位思考。
>
> > 这是一项 “修补的紧急工作”，我们最初仍然诚实地认为 “精英” 意味着 “包容”。从那以后，我们学到了很多其他东西。
> >
> > —— Benno Rice

关于文中提及的社区问题及社区的 CoC，我建议大家先去看看 linus 喷了多少次提交代码的开发者，以及他们的内核邮件列表[有多少辱骂他人的词汇](https://lore.kernel.org/lkml/YH4Aa1zFAWkITsNK@zeniv-ca.linux.org.uk/)Linux 已经说过了——The Linux community is now a dirty quagmire（泥潭）。不全文翻译了大家自己体会吧，懂的都懂。为此我专门撰写了[一篇文章](https://book.bsdcn.org/di-19-zhang-wen-xue-gu-shi/di-19.5-jie-linux-she-qu-yi-jing-cheng-wei-le-yi-ge-ang-zang-de-ni-tan.html)

> 06 结语
> 2022 年 1 月，FreeBSD 基金会制定了一份时间跨度近 5 年的[技术路线图](https://www.oschina.net/news/178599/freebsd-technology-roadmap)，决定从面向终端用户的改进（特指笔记本和台式机）、商用服务器、工具和应用和虚拟化和容器 4 个方面为重点，以扩大和增强技术团队的实力。
>
> 这份蓝图代表 FreeBSD 仍在努力朝更好的方向进发，正如 Jordan Hubbard 所说的那样，现在的 FreeBSD 应该是年轻人
> 的天下，这样才会更具活力。
>
> > 早在 1990 年代我就用过 FreeBSD，当时我没什么钱，住在政府为低收入者提供的房子里，是 FreeBSD 帮助我摆脱了贫困 —— 在雅虎找到工作是因为我会用 FreeBSD，而 WhatsApp 也是用 FreeBSD 服务器为数以亿计的用户提供服务。
> >
> > —— WhatsApp 联合创始人兼 CEO Jan Koum

我确信这才是一种回馈 BSD 的好的方式，不论是你在商业上的成功也好，还是你只是靠 BSD 养家糊口。而不止局限于所谓代码的强制开源与否、你不可否认，BSDL 为商业公司快速发展提供了不竭的动力。而最终，商业公司也会回馈于 BSD，而这不是出于强制性或者是可怜 BSD，这同样是出于商用利益考量，将商业公司所需的基础注入到 BSD 系统中，会使得他们的开发迭代更加高效，FreeBSD 的开发者也乐意这样做。而不是让人看着就很难受，有代码却因为许可证原因不能复用，又去造无用的轮子。

你必须承认这个世界是由利益驱动的，因此 FreeBSD 绝不是错误的使用了一种错误的许可证，而这是为了真正的自由，为了更加远大的理想——让所有人不受限的在最大利益上使用 FreeBSD 的代码。这才是自由软件运动真正的目标。BSDL 给了人们最大的自由，而不是让人们想着如何逃避 GPL，如何再去重复造轮子，浪费人力物力。

GPL 在实际上严重阻碍了代码复用，产生了大量不利于环境保护的垃圾。从这个观点来看，阻碍生态环境良性循环是 GPL 的阿喀琉斯之踵。

> 不管 FreeBSD 这盘棋下得多么艰难、多么不得势，但它给世界带来的一切是如此精彩。
