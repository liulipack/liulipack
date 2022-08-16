# 准备

## 样式调整

**字体**
请手动安装 [Noto Sans Mono CJK SC-Regular(无虚缺字黑体等宽中国大陆地区-普宽)](https://github.com/googlefonts/noto-cjk/raw/main/Sans/Mono/NotoSansMonoCJKsc-Regular.otf) 字体。

**油猴脚本**
请手动安装油猴类插件，新建脚本，并填入以下脚本：
```JavaScript
// ==UserScript==
// @name         GitHub_自述优化
// @name:zh-CN   GitHub_自述优化
// @description  为 LiuliPack/liulipack 仓库修改样式、修正潜在的安全问题。
// @version      0.1
// @author       LiuliPack
// @namespace    https://github.com/liulipack/UserScript
// @license      WTFPL
// @match        https://github.com/liulipack/liulipack/blob/main/README-Full.md
// @grant        GM_addStyle
// @run-at       document-end
// ==/UserScript==

'use strict';

// 修改样式。
GM_addStyle('/*蒙版*/#readme span:not(.highlight span),#readme span a{background-color:#000;color:#000}#readme span:hover:not(.highlight span),#readme span:hover a{color:#fff;transition:color .15s cubic-bezier(.40,.00,1.00,1.00)}#readme span:hover a{color:var(--color-accent-fg)}/*字体*/.markdown-body,pre{font-family:\'Noto Sans Mono CJK SC\'}/*隐藏*/.markdown-body>:nth-child(-n+5){display:none}.markdown-body>:nth-child(6){margin-top:0!important}');

// 修正潜在的链接安全问题。
document.querySelectorAll('a[href]').forEach((link) => {
    const regex = new RegExp('(gist.)?github.com');
    if(!regex.test(link.href)) {
        link.setAttribute('target','_blank');
        link.setAttribute('rel','nofollow noopener noreferrer');
    }
});
```

# 我是谁
始于2019年4月4日的“黄色废料”。

# 我在哪(可公开)
- 常用
  - [琉璃神社](https://www.hacg.cat/wp/bbs/profile/76554) - [社区](https://www.hacg.me/wp/bbs)
  - [灵梦广场](https://acg.is/u/LiuliPack) - [求助板块](https://acg.is/t/wanted)
  - [Gmail](mailto:liulipack@gmail.com)
- 低频
  - [哔哩哔哩](https://space.bilibili.com/2091925785)
  - [YouTube](https://www.youtube.com/channel/UCFZdUtZ7p4OZLW-HkBF1oXA)
  - [GitHub](https://github.com/liulipack)
  - [Nyaa-sukebei](https://sukebei.nyaa.si/user/liulipack)
  - [Twitter](https://twitter.com/liulipack)
- 占位
  - [萌幻之乡](https://www.hmoe11.net/author/732546) - 鹰小队之前有在这投过稿。
  - [绅士仓库](https://cangku.io/user/292049/post) - 之前神社有人问能不能访问。
  - [bangumi-废弃、新账号](https://bgm.tv/user/631093) - 忘记之前有注册过。尝试和站长联系把号合并，但并未理睬。
  - [喵子小屋](https://forum.h3dhub.com/space-uid-37585.html) - 喵子字幕组当初在神社有投过稿就顺手注册了。<span class="mask">商业气息太重不想待。</span>
  - [bangumi](https://bgm.tv/user/544460) - 使用 AniDB 代替。
  - [Facebook](https://www.facebook.com/profile.php?id=100069540391908) - 弃用。后续内容在 Twitter 更新。
  - [南+](https://south-plus.net/u.php?uid-1419056.html) - [询问&求物板块](https://south-plus.net/thread.php?fid=48#c) - 弃用。桜都不更里番，待着也没意义。

# 我在干什么

## 未来
- [ ] 购买一台树莓派或香橙派、固态硬盘和移动电源用于保种，并制作相关教程。
- [ ] 完全掌握日语，更好地译制动画。
- [ ] 完全掌握一项编程语言。

## 现在
- 我在[鹰小队翻译组](https://taka-sub.github.io)、[魔穗字幕组](https://sukebei.nyaa.si/user/Maho-subs)和[極彩花夢字幕组](https://kyokusai.com)无偿制作动画时间轴和一般压制；~~YuiStar 字幕组时间轴和一般压制<span class="mask">他们还在用着我早就弃用的某 IM 软件，回去的话不知道还能不能认我是组员...</span>；~~
- 新人视频作者；
- 我在琉璃神社和灵梦广场提供无偿帮助；
- [琉璃神社壁纸包保种者](HACGWallpaperSet.md)；<span class="mask">如果安装了`样式调整`脚本请新建页面打开它。</span>
- 番茄工作法践行者。当我没说

## 过去

### 2022年
**08月16日 [+]** 为鹰小队完成部分(10:20/16:13)《[OVA 聖華女学院公認竿おじさん ＃4 金髪爆乳生徒会長ルイーザ・リヒター](http://www.getchu.com/soft.phtml?id=1177912)》的待校对字幕。  
**08月11日 [+]** 为極彩花夢完成部分(05:17/28:30)《[搾精病棟 THE ANIMATION ～タチバナ編～](http://www.getchu.com/soft.phtml?id=1122386)仓库完成空白时轴。  
**08月13日 [~]** 打算离开除魔穗外的字幕组、翻译组，自建 [Pure-Timing](https://github.com/liulipack/Pure-Timing) 仓库完成空白时轴。  
**08月08日 [+]** 为鹰小队完成《[聖○○学園2 ～後編～ 剥奪された権力](http://www.getchu.com/soft.phtml?id=1185400)》的空白字幕。<span class="mask">你没看错，是空轴。翻译内容质量太差，恰好又碰上重叠对话特别多的作品。在经过组长同意后做了空轴。</span>  
**08月07日 [+]** 为極彩花夢完成《[ハヂ＋ ～晒される羞チ心～](http://www.getchu.com/soft.phtml?id=1179246)》的空白字幕。  
**08月03日 [+]** 为 [@DeXiao](https://github.com/De-Xiao) 完成《[契约之吻](https://engage-kiss.com/bddvd/)》S01E04 的部分待校对字幕。  
**08月02日 [+]** 为鹰小队完成《[搾精病棟 THE ANIMATION 第2巻 ～クロカワ編～](http://www.getchu.com/soft.phtml?id=1179049)》的待校对字幕<span class="mask">基于極彩花夢的空轴</span>；为極彩花夢完成《[ＳＵＭＭＥＲ 〜田舎の性活〜　第一話　日焼けの跡とスクール水着](http://www.getchu.com/soft.phtml?id=1186757)》的空白字幕。  
**07月31日 [+]** 为極彩花夢完成《[コンビニ少女Z 第四話 あなた、コンビニマネですよね。本社に万引きがバレていいんですか？](http://www.getchu.com/soft.phtml?id=1179245)》的空白字幕。  
**07月31日 [+]** 为極彩花夢完成《[搾精病棟 THE ANIMATION 第2巻 ～クロカワ編～](http://www.getchu.com/soft.phtml?id=1179049)》的空白字幕。  
**07月28日 [+]** 为極彩花夢完成《[夏休み明けの彼女は・・・前編](http://www.getchu.com/soft.phtml?id=1177159)》的空白字幕。  
**07月27日 [+]** 为極彩花夢完成《[ハーレム・カルト 2 side HAREM［宇場義行］](http://www.getchu.com/soft.phtml?id=1170140)》的空白字幕。  
**07月26日 [+]** 为極彩花夢完成《[ハーレム・カルト 1 side HAREM［宇場義行］](http://www.getchu.com/soft.phtml?id=1170139)》的空白字幕。<span class="mask">搞错了，白忙活</span>  
**07月23日 [+]** 为極彩花夢完成《[JK限界交尾 ～合意挿入でバチバチ肉穴化～ 第1話 性活部へようこそ](http://www.getchu.com/soft.phtml?id=1177158)》的空白字幕。  
**07月22日 [+]** 为極彩花夢完成《[ツグナヒ 高飛車お姫様・瑠璃子～はじまりの痴激～](http://www.getchu.com/soft.phtml?id=1174716)》的空白字幕。  
**07月20日 [+]** 加入[極彩花夢](https://kyokusai.com)。根据 Nyaa 相关资源页信息加入了聊天群组，看到组长抱怨。在私聊表明可以无偿帮忙被拒后，成为组员；为極彩花夢完成《[エロ医師 清純ドエロ・綾乃～漲る好奇芯～](http://www.getchu.com/soft.phtml?id=1174717)》的空白字幕。  
**07月15日 [+]** 为鹰小队完成《[OVA 聖華女学院公認竿おじさん ＃2 陸上少女 加藤美桜](http://www.getchu.com/soft.phtml?id=1177910)》的待校对字幕。  
**07月12日 [+]** 为鹰小队完成《[OVA 聖華女学院公認竿おじさん ＃1 黒髪清楚お嬢様 如月巴](http://www.getchu.com/soft.phtml?id=1177909)》的待校对字幕。  
**07月11日 [+]** 为魔穗完成《[やみつきフェロモン THE ANIMATION 第2巻](http://www.getchu.com/soft.phtml?id=1155604)》的待校对字幕。  
**07月10日 [+]** 为魔穗完成《[やみつきフェロモン THE ANIMATION 第1巻](http://www.getchu.com/soft.phtml?id=1155603)》的待校对字幕。  
**06月21日 [+]** 完成《[オタクに優しいギャルとか、巨乳の幼なじみとか。 2 [ふみひこ]](http://www.getchu.com/soft.phtml?id=1157929)》的待校对字幕。  
**06月05日 [+]** 完成《[OVA巨乳女戦士・土下座○○ ＃1](http://www.getchu.com/soft.phtml?id=1173203)》的待校对字幕。  
**05月30日 [+]** 完成《[コスプレチェンジ～ピュア系女子大生の危険な性癖～ 第二話 巨乳女子大生がコスプレ七変化!?疑惑の取り調べ室で手錠拘束プレイ](http://www.getchu.com/soft.phtml?id=1155732)》的待校对字幕。  
**05月24日 [+]** 完成《[OVA 巨乳エルフ母娘○○ ＃2 女王と姫の快楽調教。守護騎士は○○に沈む](http://www.getchu.com/soft.phtml?id=1154466)》的待校对字幕。<span class="mask">不实用。短短16分钟，塞下了四位女性角色和片尾。</span>  
**05月20日 [+]** 加入魔穗字幕组。此前就想加入魔穗，在御所正好看到[招募信息](https://blog.reimu.net/archives/74531)就入组了；完成《[OVA 巨乳エルフ母娘○○ ＃1 エルフの国を蹂躙する男。汚された女王と姫](http://www.getchu.com/soft.phtml?id=1154455)》的待校对字幕。  
**05月15日 [+]** 完成《[OVA ○○性指導 ＃5](http://www.getchu.com/soft.phtml?id=1159399)》《[OVA ○○性指導 ＃6](http://www.getchu.com/soft.phtml?id=1159400)》的字幕修正。<span class="mask">等待繁体化版本制作完成一同发布。</span>  
**05月13日 [+]** 完成《[OVA ○○性指導 ＃6](http://www.getchu.com/soft.phtml?id=1159400)》的待校对字幕。  
**05月07日 [+]** 完成《[OVA ○○性指導 ＃5](http://www.getchu.com/soft.phtml?id=1159399)》的待校对字幕。<span class="mask">我们却校对和繁化，但我不会日语，不知道怎么考核...</span>创建 [liulipack/blank-timing](https://github.com/liulipack/blank-timing) 仓库，存储空白时轴。  
**04月07日 [+]** 完成《[うさみみボウケンタン～セクハラしながら世界を救え～ 第四話 最終決戦！勇者と精霊は結ばれ、想いは受け継がれる](http://www.getchu.com/soft.phtml?id=1163795)》《[エロ医師 ワイセツチン療・綾乃＆怜奈～ちょろハメ危嬉いっぱつ～](https://www.getchu.com/soft.phtml?id=1163797)》的待校对字幕。  
**03月31日 [+]** 完成《[○○交配 第五話 内気な彼女は人魚の歌姫](http://www.getchu.com/soft.phtml?id=1163796)》的待校对字幕。  
**03月30日 [+]** 完成《[Abandon ‐100ヌキしないと出られない不思議な教室‐ 第1話 闇のSEXゲーム](http://www.getchu.com/soft.phtml?id=1150003)》的待校对字幕。  
**02月25日 [+]** 完成《[OVA 茜ハ摘マレ染メラレル ＃2](http://www.getchu.com/soft.phtml?id=1154468)》的空白时轴。  
**02月23日 [+]** 完成《[OVA 茜ハ摘マレ染メラレル ＃1](http://www.getchu.com/soft.phtml?id=1154467)》的空白时轴。  
**02月11日 [+]** Minecraft Java Edition 1.8.* 类 2B2T 服务器完工。(已关服)  
**02月04日 [+]** 完成《[エロ医師 清純無垢っつり・綾乃～不純診察中ズリ触診～](http://www.getchu.com/soft.phtml?id=1155733)》的待校对字幕。  
**02月02日 [+]** 完成《[OVA 巨乳エルフ母娘催眠 ＃1 エルフの国を蹂躙する男。汚された女王と姫](http://www.getchu.com/soft.phtml?id=1154455)》的待校对字幕。<span class="mask">我们还在。</span>  

### 2021年
**全年总结 [~]** 通过 qBittorrent 统计分享率达 5.67；5月3日至12月31日共完成 28 部动画待校对字幕；在琉璃神社社区、灵梦广场和南+求助板块完成 1660(琉璃神社社区 1599 次，灵梦广场 22 次，南+求助板块 39 次) 次回复，其中灵梦广场和南+经过详细对比完全为帮扶性回复，琉璃神社社区包含部分聊天类回复；完成 3 期《CSGO 高光时刻》系列作品，搬运 3 部他人作品至国际互联网平台并署名；完成 H 萌娘的2021年4月至10月里番合集页面编辑。  
**12月30日 [+]** 完成《[サキュバスアプリ ～学園催眠～ 第3話[溝口ぜらちん]](http://www.getchu.com/soft.phtml?id=1154039)》的待校对字幕。  
**12月23日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃5](http://www.getchu.com/soft.phtml?id=1140071)》的待校对字幕。  
**12月22日 [+]** 完成《[身体で解決 百鬼屋探偵事務所 ～百鬼屋 光の妖怪事件簿～ 第四話 妖怪大戦争復讐劇](http://www.getchu.com/soft.phtml?id=1147808)》的待校对字幕。<span class="mask">结尾那段强行关联《金田一》，太搞了。</span>  
**12月21日 [+]** 完成《[コスプレチェンジ～ピュア系女子大生の危険な性癖～ 第一話 巨乳女子大生がコスプレ七変化!?魅惑の妖怪探偵にムチエロチェンジ](http://www.getchu.com/soft.phtml?id=1147809)》的待校对字幕。<span class="mask">作为里番它不实用，作为表里番它很省钱。总结，别看。</span>  
**12月14日 [+]** 完成《[ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 下巻](http://www.getchu.com/soft.phtml?id=1147555)》的待校对字幕。  
**12月10日 [+]** 完成《[ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 上巻](http://www.getchu.com/soft.phtml?id=1147554)》的待校对字幕。  
**12月05日 [+]** 完成《[初めてのヒトヅマ 第3話 デリバリーセックス](http://www.getchu.com/soft.phtml?id=1148637)》的待校对字幕。<span class="mask">[不应期](https://zh.wikipedia.org/wiki/不应期_(性))打轴就是快。</span>  
**12月04日 [+]** 完成《[そしてわたしはセンセイに…… ～脇の下のアイツ……～](http://www.getchu.com/soft.phtml?id=1147807)》的待校对字幕。  
**11月29日 [+]** 完成《[ビッチな淫姉さまぁ ＃4[TYPE.90]](http://www.getchu.com/soft.phtml?id=1146141)》的待校对字幕。  
**11月25日 [+]** 通过[幻城字幕组动态](https://t.bilibili.com/596955790783806461)，成功加入 YuiStar 字幕组。  
**11月23日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃3](http://www.getchu.com/soft.phtml?id=1140069)》的待校对字幕。  
**11月18日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃4](http://www.getchu.com/soft.phtml?id=1140070)》的待校对字幕。  
**11月16日 [+]** 完成《[オナホ教室 ～女子全員妊娠計画～ THE ANIMATION](http://www.getchu.com/soft.phtml?id=1144249)》的待校对字幕。  
**11月10日 [+]** 完成《[そしてわたしはおじさんに…… ～揺蕩う食い込み～](http://www.getchu.com/soft.phtml?id=1145525 )》的待校对字幕。  
**11月07日 [+]** 完成《[家属～母と姉妹の嬌声～ 疼き逸る媚肉・乙葉～揺られ搾られ姉痴漢～](http://www.getchu.com/soft.phtml?id=1145526)》的待校对字幕。  
**11月05日 [+]** 完成《[うさみみボウケンタン～セクハラしながら世界を救え～ 第二話 可愛いあの娘は新たな刺客！ 無人島のセクハラ暮らし](http://www.getchu.com/soft.phtml?id=1145524)》的待校对字幕。<span class="mask">是我的问题，还是翻译的问题？总感觉怪怪的。</span>  
**10月26日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃2](http://www.getchu.com/soft.phtml?id=1140068)》的待校对字幕。<span class="mask">某句对话里，藏了个彩蛋。不知道正式时轴还在不在。</span>  
**10月25日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃1](http://www.getchu.com/soft.phtml?id=1140067)》的待校对字幕。  
**10月10日 [+]** 完成《[トイレの花子さんVS屈強退魔師 ～悪堕ちマ○コに天誅ザーメン連続中出し～ 第四怪 愕然『口裂け女』!! 爆乳露出痴女に公然わいせつ連続射精](http://www.getchu.com/soft.phtml?id=1140822)》的待校对字幕。  
**10月07日 [+]** 完成《[この会社、なにかおかしい...っ! #1](https://www.dlsite.com/maniax/work/=/product_id/RJ342701.html)》的待校对字幕。<span class="mask">我组是没其他时轴了嘛...</span>  
**10月05日 [+]** 完成《[そしてわたしはセンセイに…… ～でびゅ～ちゃん～](http://www.getchu.com/soft.phtml?id=1140823)》的待校对字幕。  
**10月02日 [+]** 完成《[この会社、なにかおかしいっ...! #2](https://www.dlsite.com/maniax/work/=/product_id/RJ342702.html)》的待校对字幕。  
**10月01日 [+]** 扩充、调整久未更新的 [liulipack/GM_script](https://github.com/liulipack/GM_script)。  
**09月20日 [+]** 完成《[OVA 邪娠娼館―淫乱巨乳母娘生贄儀式― ＃1](http://www.getchu.com/soft.phtml?id=1135329)》的待校对字幕。

# 2020年
**10月06日 [+]** 加入鹰小队字幕组。当时桜都爆出被抄袭事件，不名真相的我选择加入鹰小队。如今看来似乎是选错边了。<span class="mask">入组后也没好意思问组长具体什么情况；由于腾讯号被封的原因，导致具体时间不可考。标注时间仅为推测。</span>