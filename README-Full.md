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
GM_addStyle('/*黑幕*/#readme span:not(.highlight span),#readme span a{background-color:#000;color:#000}#readme span:hover:not(.highlight span),#readme span:hover a{color:#fff;transition:color .15s cubic-bezier(.40,.00,1.00,1.00)}#readme span:hover a{color:var(--color-accent-fg)}/*字体*/.markdown-body,pre{font-family:\'Noto Sans Mono CJK SC\'}/*隐藏*/.markdown-body>:nth-child(-n+5){display:none}.markdown-body>:nth-child(6){margin-top:0!important}');

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
始于2019年4月4日的老色批；新人视频作者；鹰小队翻译组时间轴兼临时片源、时轴、一般压制、发布；YuiStar 字幕组时间轴、压制<span class="shady">他们还在用着我早就弃用的某 IM 软件，回去的话不知道还能不能认我是组员...</span>；魔穗字幕组时轴、一般压制；[琉璃神社壁纸包保种者](HACGWallpaperSet.md)；番茄工作法践行者。

# 我在哪(可公开)
- 常用
  - [琉璃神社](https://www.hacg.cat/wp/bbs/profile/76554) - [社区](https://www.hacg.me/wp/bbs)
  - [灵梦广场](https://acg.is/u/LiuliPack) - [求助板块](https://acg.is/t/wanted)
  - [南+](https://south-plus.net/u.php?uid-1419056.html) - [询问&求物板块](https://south-plus.net/thread.php?fid=48#c)
  - [Gmail](mailto:liulipack@gmail.com)
- 低频
  - [哔哩哔哩](https://space.bilibili.com/2091925785)
  - [YouTube](https://www.youtube.com/channel/UCFZdUtZ7p4OZLW-HkBF1oXA)
  - [GitHub](https://github.com/liulipack)
  - [Nyaa-sukebei](https://sukebei.nyaa.si/user/liulipack)
  - [Facebook](https://www.facebook.com/profile.php?id=100069540391908)
  - [Twitter](https://twitter.com/liulipack)
- 占位
  - [萌幻之乡](https://www.hmoe11.net/author/732546) - 鹰小队之前有在这投过稿。
  - [绅士仓库](https://cangku.io/user/292049/post) - 之前神社有人问能不能访问。
  - [bangumi-废弃、新账号](https://bgm.tv/user/631093) - 忘记之前有注册过。尝试和站长联系把号合并，但并未理睬。
  - [喵子小屋](https://forum.h3dhub.com/space-uid-37585.html) - 喵子字幕组当初在神社有投过稿就顺手注册了。<span class="shady">商业气息太重不想待。</span>
  - [bangumi](https://bgm.tv/user/544460) - 使用 AniDB 代替。

# 我在干什么

## 未来
- [ ] 购买一台树莓派或香橙派、固态硬盘和移动电源用于保种，并制作相关教程。
- [ ] 完全掌握日语，更好地译制动画。
- [ ] 完全掌握一项编程语言。

## 现在
- 我在[鹰小队翻译组](https://taka-sub.github.io)、[魔穗字幕组](https://sukebei.nyaa.si/user/Maho-subs)和 [liulipack/blank-timing](https://github.com/liulipack/blank-timing) 无偿制作动画时间轴；
- 我在琉璃神社和灵梦广场提供无偿帮助；
- 我在无偿维护多个 GitHub 仓库；
- 我在创作视频。

## 过去

### 2022年
**05月20日 [+]** 加入魔穗字幕组；完成《[OVA 巨乳エルフ母娘○○ ＃1 エルフの国を蹂躙する男。汚された女王と姫](http://www.getchu.com/soft.phtml?id=1154455)》的待校对时轴。  
**05月15日 [+]** 完成《[OVA ○○性指導 ＃5](http://www.getchu.com/soft.phtml?id=1159399)》《[OVA ○○性指導 ＃6](http://www.getchu.com/soft.phtml?id=1159400)》的字幕修正。<span class="shady">等待繁体化版本制作完成一同发布。</span>  
**05月13日 [+]** 完成《[OVA ○○性指導 ＃6](http://www.getchu.com/soft.phtml?id=1159400)》的待校对时轴。  
**05月07日 [+]** 完成《[OVA ○○性指導 ＃5](http://www.getchu.com/soft.phtml?id=1159399)》的待校对时轴；<span class="shady">我们却校对和繁化，但我不会日语，不知道怎么考核...</span>创建 [liulipack/blank-timing](https://github.com/liulipack/blank-timing) 仓库，存储空白时轴。  
**04月07日 [+]** 完成《[うさみみボウケンタン～セクハラしながら世界を救え～ 第四話 最終決戦！勇者と精霊は結ばれ、想いは受け継がれる](http://www.getchu.com/soft.phtml?id=1163795)》《[エロ医師 ワイセツチン療・綾乃＆怜奈～ちょろハメ危嬉いっぱつ～](https://www.getchu.com/soft.phtml?id=1163797)》的待校对时轴。  
**03月31日 [+]** 完成《[○○交配 第五話 内気な彼女は人魚の歌姫](http://www.getchu.com/soft.phtml?id=1163796)》的待校对时轴。  
**03月30日 [+]** 完成《[Abandon ‐100ヌキしないと出られない不思議な教室‐ 第1話 闇のSEXゲーム](http://www.getchu.com/soft.phtml?id=1150003)》的待校对时轴。  
**02月25日 [+]** 完成《[OVA 茜ハ摘マレ染メラレル ＃2](http://www.getchu.com/soft.phtml?id=1154468)》的空白时轴。  
**02月23日 [+]** 完成《[OVA 茜ハ摘マレ染メラレル ＃1](http://www.getchu.com/soft.phtml?id=1154467)》的空白时轴。  
**02月11日 [+]** Minecraft Java Edition 1.8.* 类 2B2T 服务器完工。(50.93.205.138:25566)  
**02月04日 [+]** 完成《[エロ医師 清純無垢っつり・綾乃～不純診察中ズリ触診～](http://www.getchu.com/soft.phtml?id=1155733)》的待校对时轴。  
**02月02日 [+]** 完成《[OVA 巨乳エルフ母娘催眠 ＃1 エルフの国を蹂躙する男。汚された女王と姫](http://www.getchu.com/soft.phtml?id=1154455)》的待校对时轴。<span class="shady">我们还在。</span>  

### 2021年
**全年总结 [~]** 通过 qBittorrent 统计分享率达 5.67；5月3日至12月31日共完成 28 部动画待校对时轴；在琉璃神社社区、灵梦广场和南+求助板块完成 1660(琉璃神社社区 1599 次，灵梦广场 22 次，南+求助板块 39 次) 次回复，其中灵梦广场和南+经过详细对比完全为帮扶性回复，琉璃神社社区包含部分聊天类回复；完成 3 期《CSGO 高光时刻》系列作品，搬运 3 部他人作品至国际互联网平台并署名；完成 H 萌娘的2021年4月至10月里番合集页面编辑。  
**12月30日 [+]** 完成《[サキュバスアプリ ～学園催眠～ 第3話[溝口ぜらちん]](http://www.getchu.com/soft.phtml?id=1154039)》的待校对时轴。  
**12月23日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃5](http://www.getchu.com/soft.phtml?id=1140071)》的待校对时轴。  
**12月22日 [+]** 完成《[身体で解決 百鬼屋探偵事務所 ～百鬼屋 光の妖怪事件簿～ 第四話 妖怪大戦争復讐劇](http://www.getchu.com/soft.phtml?id=1147808)》的待校对时轴。<span class="shady">结尾那段强行关联《金田一》，太搞了。</span>  
**12月21日 [+]** 完成《[コスプレチェンジ～ピュア系女子大生の危険な性癖～ 第一話 巨乳女子大生がコスプレ七変化!?魅惑の妖怪探偵にムチエロチェンジ](http://www.getchu.com/soft.phtml?id=1147809)》的待校对时轴。<span class="shady">作为里番它不实用，作为表里番它很省钱。总结，别看。</span>  
**12月14日 [+]** 完成《[ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 下巻](http://www.getchu.com/soft.phtml?id=1147555)》的待校对时轴。  
**12月10日 [+]** 完成《[ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 上巻](http://www.getchu.com/soft.phtml?id=1147554)》的待校对时轴。  
**12月05日 [+]** 完成《[初めてのヒトヅマ 第3話 デリバリーセックス](http://www.getchu.com/soft.phtml?id=1148637)》的待校对时轴。<span class="shady">[不应期](https://zh.wikipedia.org/wiki/不应期_(性))打轴就是快。</span>  
**12月04日 [+]** 完成《[そしてわたしはセンセイに…… ～脇の下のアイツ……～](http://www.getchu.com/soft.phtml?id=1147807)》的待校对时轴。  
**11月29日 [+]** 完成《[ビッチな淫姉さまぁ ＃4[TYPE.90]](http://www.getchu.com/soft.phtml?id=1146141)》的待校对时轴。  
**11月25日 [+]** 通过[幻城字幕组动态](https://t.bilibili.com/596955790783806461)，成功加入 YuiStar 字幕组。  
**11月23日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃3](http://www.getchu.com/soft.phtml?id=1140069)》的待校对时轴。  
**11月18日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃4](http://www.getchu.com/soft.phtml?id=1140070)》的待校对时轴。  
**11月16日 [+]** 完成《[オナホ教室 ～女子全員妊娠計画～ THE ANIMATION](http://www.getchu.com/soft.phtml?id=1144249)》的待校对时轴。  
**11月10日 [+]** 完成《[そしてわたしはおじさんに…… ～揺蕩う食い込み～](http://www.getchu.com/soft.phtml?id=1145525 )》的待校对时轴。  
**11月07日 [+]** 完成《[家属～母と姉妹の嬌声～ 疼き逸る媚肉・乙葉～揺られ搾られ姉痴漢～](http://www.getchu.com/soft.phtml?id=1145526)》的待校对时轴。  
**11月05日 [+]** 完成《[うさみみボウケンタン～セクハラしながら世界を救え～ 第二話 可愛いあの娘は新たな刺客！ 無人島のセクハラ暮らし](http://www.getchu.com/soft.phtml?id=1145524)》的待校对时轴。<span class="shady">是我的问题，还是翻译的问题？总感觉怪怪的。</span>  
**10月26日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃2](http://www.getchu.com/soft.phtml?id=1140068)》的待校对时轴。<span class="shady">某句对话里，藏了个彩蛋。不知道正式时轴还在不在。</span>  
**10月25日 [+]** 完成《[OVA 千鶴ちゃん開発日記 ＃1](http://www.getchu.com/soft.phtml?id=1140067)》的待校对时轴。  
**10月10日 [+]** 完成《[トイレの花子さんVS屈強退魔師 ～悪堕ちマ○コに天誅ザーメン連続中出し～ 第四怪 愕然『口裂け女』!! 爆乳露出痴女に公然わいせつ連続射精](http://www.getchu.com/soft.phtml?id=1140822)》的待校对时轴。  
**10月07日 [+]** 完成《[この会社、なにかおかしい...っ! #1](https://www.dlsite.com/maniax/work/=/product_id/RJ342701.html)》的待校对时轴。<span class="shady">我组是没其他时轴了嘛...</span>  
**10月05日 [+]** 完成《[そしてわたしはセンセイに…… ～でびゅ～ちゃん～](http://www.getchu.com/soft.phtml?id=1140823)》的待校对时轴。  
**10月02日 [+]** 完成《[この会社、なにかおかしいっ...! #2](https://www.dlsite.com/maniax/work/=/product_id/RJ342702.html)》的待校对时轴。  
**10月01日 [+]** 扩充、调整久未更新的 [liulipack/GM_script](https://github.com/liulipack/GM_script)。  
**09月20日 [+]** 完成《[OVA 邪娠娼館―淫乱巨乳母娘生贄儀式― ＃1](http://www.getchu.com/soft.phtml?id=1135329)》的待校对时轴。

<!--
# WikiText(Wiki 语法)

```
== 我是谁 ==
始于2019年4月4日的老鬼畜。鹰小队翻译组时间轴；YuiStar 字幕组时间轴、压制；Github [https://github.com/liulipack/awesome-hentai awesome-hentai] 仓库创建者；番茄工作法践行者。

== 我在哪 ==
*常用
**[https://www.hacg.cat/wp/bbs/profile/76554 琉璃神社] - [https://www.hacg.me/wp/bbs 社区]
**[https://acg.is/u/LiuliPack 灵梦广场] - [https://acg.is/t/wanted 求助板块]
**[https://south-plus.net/u.php?uid-1419056.html 南+] - [https://south-plus.net/thread.php?fid=48#c 询问&求物板块]
**[mailto:liulipack@gmail.com Gmail]
*低频
**[https://space.bilibili.com/2091925785 哔哩哔哩]
**[https://www.youtube.com/channel/UCFZdUtZ7p4OZLW-HkBF1oXA YouTube]
**[https://github.com/liulipack GitHub]
**[https://sukebei.nyaa.si/user/liulipack Nyaa-sukebei]
**[https://www.facebook.com/profile.php?id=100069540391908 Facebook]
**[https://twitter.com/liulipack Twitter]
*占位
**[https://www.hmoe11.net/author/732546 萌幻之乡] - 鹰小队之前有在这投过稿。
**[https://cangku.io/user/292049/post 绅士仓库] - 之前神社有人问能不能访问。
**[https://bgm.tv/user/631093 bangumi-废弃、新账号] - 忘记之前有注册过。尝试和站长联系，把号合并但并未理睬。
**[https://forum.h3dhub.com/space-uid-37585.html 喵子小屋] - 喵子字幕组当初在神社有投过稿就顺手注册了。{{黑幕|商业气息太重不想待。}}
**[https://bgm.tv/user/544460 bangumi] - 使用 AniDB 代替。

== 我在干什么 ==

懒得重复造轮子，这部分以后只在 https://github.com/liulipack/LP-note/blob/main/About.md 更新。

=== 2022年 ===
'''04月07日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1163795 うさみみボウケンタン～セクハラしながら世界を救え～ 第四話 最終決戦！勇者と精霊は結ばれ、想いは受け継がれる]》的待校对时轴。<br>
'''03月31日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1163796 ○○交配 第五話 内気な彼女は人魚の歌姫]》的待校对时轴。<br>
'''03月30日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1150003 Abandon ‐100ヌキしないと出られない不思議な教室‐ 第1話 闇のSEXゲーム]》的待校对时轴。<br>
'''02月25日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1154468 OVA 茜ハ摘マレ染メラレル ＃2]》的空白时轴。<br>
'''02月23日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1154467 OVA 茜ハ摘マレ染メラレル ＃1]》的空白时轴。<br>
'''02月11日 [+]''' Minecraft Java Edition 1.8.* 类 2B2T 服务器完工。(50.93.205.138:25566)<br>
'''02月04日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1155733 エロ医師 清純無垢っつり・綾乃～不純診察中ズリ触診～]》的待校对时轴。<br>
'''02月02日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1154455 OVA 巨乳エルフ母娘催眠 ＃1 エルフの国を蹂躙する男。汚された女王と姫]》的待校对时轴。{{黑幕|我们还在。}}

=== 2021年 ===
'''全年总结 [~]''' 通过 qBittorrent 统计分享率达 5.67；5月3日至12月31日共完成 28 部动画待校对时轴；在琉璃神社社区、灵梦广场和南+求助板块完成 1660(琉璃神社社区 1599 次，灵梦广场 22 次，南+求助板块 39 次) 次回复，其中灵梦广场和南+经过详细对比完全为帮扶性回复，琉璃神社社区包含部分聊天类回复；完成 3 期《CSGO 高光时刻》系列作品，搬运 3 部他人作品至国际互联网平台并署名；完成 H 萌娘的2021年4月至10月里番合集页面编辑。<br>
'''12月30日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1154039 サキュバスアプリ ～学園催眠～ 第3話[溝口ぜらちん]]》的待校对时轴。<br>
'''12月23日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140071 OVA 千鶴ちゃん開発日記 ＃5]》的待校对时轴。<br>
'''12月22日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1147808 身体で解決 百鬼屋探偵事務所 ～百鬼屋 光の妖怪事件簿～ 第四話 妖怪大戦争復讐劇]》的待校对时轴。{{黑幕|结尾那段强行关联《金田一》，太搞了。}}<br>
'''12月21日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1147809 コスプレチェンジ～ピュア系女子大生の危険な性癖～ 第一話 巨乳女子大生がコスプレ七変化!?魅惑の妖怪探偵にムチエロチェンジ]》的待校对时轴。{{黑幕|作为里番它不实用，作为表里番它很省钱。总结，别看。}}<br>
'''12月14日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1147555 ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 下巻]》的待校对时轴。<br>
'''12月10日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1147554 ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 上巻]》的待校对时轴。<br>
'''12月05日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1148637 初めてのヒトヅマ 第3話 デリバリーセックス]》的待校对时轴。{{黑幕|[https://zh.wikipedia.org/wiki/不应期_(性) 不应期]打轴就是快。}}<br>
'''12月04日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1147807 そしてわたしはセンセイに…… ～脇の下のアイツ……～]》的待校对时轴。<br>
'''11月29日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1146141 ビッチな淫姉さまぁ ＃4[TYPE.90]]》的待校对时轴。<br>
'''11月25日 [+]''' 通过[https://t.bilibili.com/596955790783806461 幻城字幕组动态]，成功加入 YuiStar 字幕组。<br>
'''11月23日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140069 OVA 千鶴ちゃん開発日記 ＃3]》的待校对时轴。<br>
'''11月18日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140070 OVA 千鶴ちゃん開発日記 ＃4]》的待校对时轴。<br>
'''11月16日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1144249 オナホ教室 ～女子全員妊娠計画～ THE ANIMATION]》的待校对时轴。<br>
'''11月10日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1145525 そしてわたしはおじさんに…… ～揺蕩う食い込み～]》的待校对时轴。<br>
'''11月07日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1145526 家属～母と姉妹の嬌声～ 疼き逸る媚肉・乙葉～揺られ搾られ姉痴漢～]》的待校对时轴。<br>
'''11月05日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1145524 うさみみボウケンタン～セクハラしながら世界を救え～ 第二話 可愛いあの娘は新たな刺客！ 無人島のセクハラ暮らし]》的待校对时轴。{{黑幕|是我的问题，还是翻译的问题？总感觉怪怪的。}}<br>
'''10月26日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140068 OVA 千鶴ちゃん開発日記 ＃2]》的待校对时轴。{{黑幕|某句对话里，藏了个彩蛋。不知道正式时轴还在不在。}}<br>
'''10月25日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140067 OVA 千鶴ちゃん開発日記 ＃1]》的待校对时轴。<br>
'''10月10日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140822 トイレの花子さんVS屈強退魔師 ～悪堕ちマ○コに天誅ザーメン連続中出し～ 第四怪 愕然『口裂け女』!! 爆乳露出痴女に公然わいせつ連続射精]》的待校对时轴。<br>
'''10月07日 [+]''' 完成《[https://www.dlsite.com/maniax/work/=/product_id/RJ342701.html この会社、なにかおかしい...っ! #1]》的待校对时轴。{{黑幕|我组是没其他时轴了嘛...}}<br>
'''10月05日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1140823 そしてわたしはセンセイに…… ～でびゅ～ちゃん～]》的待校对时轴。<br>
'''10月02日 [+]''' 完成《[https://www.dlsite.com/maniax/work/=/product_id/RJ342702.html この会社、なにかおかしいっ...! #2]》的待校对时轴。<br>
'''10月01日 [+]''' 扩充、调整久未更新的 [https://github.com/liulipack/GM_script liulipack/GM_script]。<br>
'''09月20日 [+]''' 完成《[http://www.getchu.com/soft.phtml?id=1135329 OVA 邪娠娼館―淫乱巨乳母娘生贄儀式― ＃1]》的待校对时轴。

<!- - 样式修改 - ->
{{背景图片|url=Impression,_Sunrise.jpg}}
```

# HTML

```HTML
<style>
/* 黑幕 */
.shady, .shady a {background-color: #000;color: #000}
.shady:hover, .shady:hover a {color: #fff;transition: color .15s cubic-bezier(.40, .00, 1.00, 1.00)}
a, .shady:hover a {color: #304FFE}
/*
亮色
- 链接 #0A59F7
- 正向事件 #64BB5C
- 负面事件 #E84026
- 不明确事件 #E5E5E5(#19000000)
深色
- 链接 #317AF7
- 正向事件 #5BA854
- 负面事件 #D94838
- 不明确事件 #FFFFFF(#19FFFFFF)
*/
</style>

<p>同时编写 Markdown、HTML 和 Wiki 语法三个版本太麻烦了，此处将在2021年12月31日后停止更新。您可移步至 <a href="https://github.com/liulipack/LP-note/blob/main/About.md" rel="nofollow noreferrer noopener" target="_blank">github.com/liulipack/LP-note</a> 或 <a href="https://www.hmoegirl.com/index.php?title=用户:Liulipack" rel="nofollow noreferrer noopener" target="_blank">H萌娘</a> 查阅新内容。由此带来的不便敬请谅解，谢谢。</p>
<h2>我是谁</h2>
<p>始于2019年4月4日的老鬼畜。鹰小队翻译组时间轴；YuiStar 字幕组时间轴、压制；Github <a href="https://github.com/liulipack/awesome-hentai" rel="nofollow noreferrer noopener" target="_blank">awesome-hentai</a> 仓库创建者；番茄工作法践行者。</p>

<h2>我在哪</h2>
<ul>
<li>常用
    <ul>
        <li><a href="https://www.hacg.cat/wp/bbs/profile/76554" rel="nofollow noreferrer noopener" target="_blank"><a href="https://www.hacg.me/wp/bbs" rel="nofollow noreferrer noopener" target="_blank">琉璃神社</a> - 社区</a></li>
        <li><a href="https://acg.is/u/LiuliPack" rel="nofollow noreferrer noopener" target="_blank">灵梦广场</a> - <a href="https://acg.is/t/wanted" rel="nofollow noreferrer noopener" target="_blank">求助板块</a></li>
        <li><a href="https://south-plus.net/u.php?uid-1419056.html" rel="nofollow noreferrer noopener" target="_blank">南+</a> - <a href="https://south-plus.net/thread.php?fid=48#c" rel="nofollow noreferrer noopener" target="_blank">询问&求物板块</a></li>
        <li><a href="mailto:liulipack@gmail.com" rel="nofollow noreferrer noopener" target="_blank">Gmail</a></li>
    </ul>
</li>
<li>低频
    <ul>
        <li><a href="https://space.bilibili.com/2091925785" rel="nofollow noreferrer noopener" target="_blank">哔哩哔哩</a></li>
        <li><a href="https://www.youtube.com/channel/UCFZdUtZ7p4OZLW-HkBF1oXA" rel="nofollow noreferrer noopener" target="_blank">YouTube</a></li>
        <li><a href="https://github.com/liulipack" rel="nofollow noreferrer noopener" target="_blank">GitHub</a></li>
        <li><a href="https://sukebei.nyaa.si/user/liulipack" rel="nofollow noreferrer noopener" target="_blank">Nyaa-sukebei</a></li>
        <li><a href="https://www.facebook.com/profile.php?id=100069540391908" rel="nofollow noreferrer noopener" target="_blank">Facebook</a></li>
        <li><a href="https://twitter.com/liulipack" rel="nofollow noreferrer noopener" target="_blank">Twitter</a></li>
    </ul>
</li>
</ul>

<h2>我在做什么</h2>
<h3>2021年</h3>
<p>
    <b>全年总结 [~]</b> 通过 qBittorrent 统计分享率达 5.67；5月3日至12月31日共完成 28 部动画待校对时轴；在琉璃神社社区、灵梦广场和南+求助板块完成 1660(琉璃神社社区 1599 次，灵梦广场 22 次，南+求助板块 39 次) 次回复，其中灵梦广场和南+经过详细对比完全为帮扶性回复，琉璃神社社区包含部分聊天类回复；完成 3 期《CSGO 高光时刻》系列作品，搬运 3 部他人作品至国际互联网平台并署名；完成 H 萌娘的2021年4月至10月里番合集页面编辑。<br />
    <b>12月30日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1154039" rel="nofollow noreferrer noopener" target="_blank">サキュバスアプリ ～学園催眠～ 第3話[溝口ぜらちん]</a>》的待校对时轴。<br />
    <b>12月23日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140071" rel="nofollow noreferrer noopener" target="_blank">OVA 千鶴ちゃん開発日記 ＃5</a>》的待校对时轴。<br />
    <b>12月22日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1147808" rel="nofollow noreferrer noopener" target="_blank">身体で解決 百鬼屋探偵事務所 ～百鬼屋 光の妖怪事件簿～ 第四話 妖怪大戦争復讐劇</a>》的待校对时轴。<span class="shady">结尾那段强行关联《金田一》，太搞了。</span><br />
    <b>12月21日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1147809" rel="nofollow noreferrer noopener" target="_blank">コスプレチェンジ～ピュア系女子大生の危険な性癖～ 第一話 巨乳女子大生がコスプレ七変化!?魅惑の妖怪探偵にムチエロチェンジ</a>》的待校对时轴。<span class="shady">作为里番它不实用，作为表里番它很省钱。总结，别看。</span><br />
    <b>12月14日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1147555" rel="nofollow noreferrer noopener" target="_blank">ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 下巻</a>》的待校对时轴。<br />
    <b>12月10日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1147554" rel="nofollow noreferrer noopener" target="_blank">ママホリック ～魅惑のママと甘々カンケイ～ THE ANIMATION 上巻</a>》的待校对时轴。<br />
    <b>12月05日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1148637" rel="nofollow noreferrer noopener" target="_blank">初めてのヒトヅマ 第3話 デリバリーセックス</a>》的待校对时轴。<span class="shady" title="你知道的太多了"><a href="https://zh.wikipedia.org/wiki/不应期_(性)" rel="nofollow noopener noreferrer" target="_blank">不应期</a>打轴就是快。</span><br />
    <b>12月04日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1147807" rel="nofollow noreferrer noopener" target="_blank">そしてわたしはセンセイに…… ～脇の下のアイツ……～</a>》的待校对时轴。<br />
    <b>11月29日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1146141" rel="nofollow noreferrer noopener" target="_blank">ビッチな淫姉さまぁ ＃4[TYPE.90]</a>》的待校对时轴。<br />
    <b>11月25日 [+]</b> 通过<a href="https://t.bilibili.com/596955790783806461" rel="nofollow noreferrer noopener" target="_blank">幻城字幕组动态</a>，成功加入 YuiStar 字幕组。<br />
    <b>11月23日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140069" rel="nofollow noreferrer noopener" target="_blank">OVA 千鶴ちゃん開発日記 ＃3</a>》的待校对时轴。<br />
    <b>11月18日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140070" rel="nofollow noreferrer noopener" target="_blank">OVA 千鶴ちゃん開発日記 ＃4</a>》的待校对时轴。<br />
    <b>11月16日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1144249" rel="nofollow noreferrer noopener" target="_blank">オナホ教室 ～女子全員妊娠計画～ THE ANIMATION</a>》的待校对时轴。<br />
    <b>11月10日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1145525" rel="nofollow noreferrer noopener" target="_blank">そしてわたしはおじさんに…… ～揺蕩う食い込み～</a>》的待校对时轴。<br />
    <b>11月07日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1145526" rel="nofollow noreferrer noopener" target="_blank">家属～母と姉妹の嬌声～ 疼き逸る媚肉・乙葉～揺られ搾られ姉痴漢～</a>》的待校对时轴。<br />
    <b>11月05日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1145524" rel="nofollow noreferrer noopener" target="_blank">うさみみボウケンタン～セクハラしながら世界を救え～ 第二話 可愛いあの娘は新たな刺客！ 無人島のセクハラ暮らし</a>》的待校对时轴。<span class="shady" title="你知道的太多了">是我的问题，还是翻译的问题？总感觉怪怪的。</span><br />
    <b>10月26日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140068" rel="nofollow noreferrer noopener" target="_blank">OVA 千鶴ちゃん開発日記 ＃2</a>》的待校对时轴。<span class="shady" title="你知道的太多了">某句对话里，藏了个彩蛋。不知道正式时轴还在不在。</span><br />
    <b>10月25日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140067" rel="nofollow noreferrer noopener" target="_blank">OVA 千鶴ちゃん開発日記 ＃1</a>》的待校对时轴。<br />
    <b>10月10日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140822" rel="nofollow noreferrer noopener" target="_blank">トイレの花子さんVS屈強退魔師 ～悪堕ちマ○コに天誅ザーメン連続中出し～ 第四怪 愕然『口裂け女』!! 爆乳露出痴女に公然わいせつ連続射精</a>》的待校对时轴。<br />
    <b>10月07日 [+]</b> 完成《<a href="https://www.dlsite.com/maniax/work/=/product_id/RJ342701.html" rel="nofollow noreferrer noopener" target="_blank">この会社、なにかおかしい...っ! #1</a>》的待校对时轴。<span class="shady" title="你知道的太多了">我组是没其他时轴了嘛...</span><br />
    <b>10月05日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1140823" rel="nofollow noreferrer noopener" target="_blank">そしてわたしはセンセイに…… ～でびゅ～ちゃん～</a>》的待校对时轴。<br />
    <b>10月02日 [+]</b> 完成《<a href="https://www.dlsite.com/maniax/work/=/product_id/RJ342702.html" rel="nofollow noreferrer noopener" target="_blank">この会社、なにかおかしいっ...! #2</a>》的待校对时轴。<br />
    <b>10月01日 [+]</b> 扩充、调整久未更新的 <a href="https://github.com/liulipack/GM_script" rel="nofollow noreferrer noopener" target="_blank">liulipack/GM_script</a> 仓库。<br />
    <b>09月20日 [+]</b> 完成《<a href="http://www.getchu.com/soft.phtml?id=1135329" rel="nofollow noreferrer noopener" target="_blank">OVA 邪娠娼館―淫乱巨乳母娘生贄儀式― ＃1</a>》的待校对时轴。<br />
</p>
```
-->