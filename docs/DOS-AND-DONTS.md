# Do's and don'ts

These are the reasons pull requests most often came back for changes or were closed. They come from the
maintainer's reviews, and each line links an example. None of this replaces [CONTRIBUTING.md](../CONTRIBUTING.md):
it is the short list of mistakes to skip. When in doubt, ask in an issue before you build. "Thanks for asking
first" is a common reply.

## Before you start: pick the right home

| Do | Don't |
|---|---|
| Put a widget or tile that can be its own app in `addons/`, as a module card ([#704](https://jxpe.yx-sf.com/huodong/design-89869413.html), [#1086](https://rlxz.tcti.cn/qiye/forum-40040959.html), [#1226](https://rrmu.tcti.cn/anfang/photo-02477556.html)) | Build it into `launcher/`, which stays small, offline and under a size budget for 1 GB TVs ([#173](https://xfal.ai-hao123.com/shuju/template-01328797.html), [#309](https://gpfr.tcti.cn/kaifa/accessibility-17583992.html)) |
| Put a whole launcher, a restyle, a port or a big feature in your own repo, plus one row in [SHOWCASE.md](../SHOWCASE.md) ([#773](https://plfy.yx-sf.com/zhizhu/company-77206341.html), [#1229](https://dmjn.ai-hao123.com/fuwu/share-21188783.html)) | Send a 2,000-line PR to the core and hope it fits ([#1109](https://qshv.wtpuscm.cn/anli/promotion-894794.html), [#1138](https://bvjd.wtpuscm.cn/shichang/seminar-542776.html)) |
| Search open and merged PRs first, and build on what's there ([#972](https://www.seomatrix.pro/index.html), [#1279](https://xjmv.yx-sf.com/yunying/team-02871108.html)) | Add a second key, map or add-on for something main already does: two would fight ([#864](https://tphq.yx-sf.com/pingce/ebook-58496158.html), [#1173](https://oavf.ai-hao123.com/guanjianci/products-68744933.html), [#1288](https://abpf.tcti.cn/wenzhang/data-11599028.html), [#271](https://nmdm.wtpuscm.cn/wendang/visitor-417416.html)) |
| Send one idea per PR, and split the rest out ([#326](https://cgfe.tcti.cn/yingxiao/reporting-40195357.html), [#488](https://fknd.ai-hao123.com/youhua/workshop-45718307.html), [#1235](https://oahd.tcti.cn/xuexi/online-23880040.html)) | Mix a TV list, a launcher change and a theme in one PR ([#268](https://dmjn.ai-hao123.com/fuwu/share-21188783.html), [#325](https://mpht.tcti.cn/yunsuan/button-61673970.html)) |

## Never, anywhere

- **No uninstalling, root or bypasses.** Everything here disables with `pm disable-user`, so `tools/restore.sh`
  undoes it. No `pm uninstall`, no `pm hide` without its undo, no root, and no way around a maker's install
  block ([#706](https://bcsl.ai-hao123.com/yunying/chapter-07416166.html), [#472](https://jnjw.ai-hao123.com/hezuo/webinar-17104581.html),
  [#678](https://xugq.ai-hao123.com/zhinan/digital-02360650.html), [#830](https://zqsc.tcti.cn/yunsuan/tactic-55734153.html),
  [#347](https://vpnr.ai-hao123.com/yunying/blog-95734007.html)).
- **No prebuilt binaries.** No APKs (not even as workflow artifacts), `.so` files or zip uploads: everyone builds
  from source ([#761](https://hlfi.yx-sf.com/zhinan/research-77781822.html), [#398](https://wzzi.yx-sf.com/chuangxin/segment-63960098.html),
  [#637](https://sojq.wtpuscm.cn/youhua/funnel-407202.html), [#1298](https://obcn.ai-hao123.com/zixun/accessibility-39960050.html)).
- **No self-updaters or release signing** ([#143](https://blya.ai-hao123.com/shichang/tag-11130864.html), [#978](https://wcty.yx-sf.com/tuiguang/management-21624714.html)).
- **No personal details.** No LAN IPs, Wi-Fi names, your own city or your own dock in shared files
  ([#25](https://nlkm.tcti.cn/shichang/domain-70840657.html), [#268](https://meod.wtpuscm.cn/kuangjia/folder-833115.html),
  [#1212](https://gpfr.tcti.cn/kaifa/accessibility-17583992.html), [#312](https://qxmm.wtpuscm.cn/jiaocheng/technology-848215.html)). Blur them in screenshots.
- **No CI or workflow edits** that come along with a feature. An invalid workflow stops every build
  ([#1265](https://jnjw.ai-hao123.com/hezuo/webinar-17104581.html), [#1298](https://zqsc.tcti.cn/yunsuan/tactic-55734153.html), [#513](https://xzqz.yx-sf.com/wenzhang/business-80874368.html)).
- **No agent or tool config.** Don't commit `.claude/`, `.codex/`, `.cursor/` hooks or similar: they run
  commands for anyone who opens the repo ([#286](https://tyiu.tcti.cn/zixun/platform-92254644.html)).
- **No logging of key presses.** It turns logcat into a keystroke log ([#176](https://ygbk.wtpuscm.cn/anli/management-258259.html)).
- **No leaving ADB open.** Nothing should keep network ADB listening after a reboot ([#877](https://rmjv.yx-sf.com/peixun/loyalty-91885850.html)).

## Debloat lists (`examples/`)

| Do | Don't |
|---|---|
| List only packages you disabled and lived with for a few days, with the model, Android version, firmware and a dated `Status:` line ([#228](https://fknd.ai-hao123.com/youhua/workshop-45718307.html), [#286](https://nmdm.wtpuscm.cn/wendang/visitor-417416.html)) | Leave the template's draft line in, or name a different TV in the header than the one you tested ([#228](https://aamt.ai-hao123.com/fuwu/support-78089670.html)) |
| Fold a TV on the same firmware into the existing folder as a second unit ([#1085](https://jzws.wtpuscm.cn/gongsi/affordable-183110.html), [#1148](https://www.ebrkdiy.cn/keji/ai-52559593.html), [#1210](https://bqcb.ai-hao123.com/fenxi/logo-05696267.html)) | Open a new folder for the same build, or rename an existing one ([#228](https://dyru.ai-hao123.com/chanpin/local-58395937.html), [#800](https://rrmu.tcti.cn/anfang/photo-02477556.html)) |
| Comment out firmware updaters, with a note that owners can turn them off ([#1306](https://houd.yx-sf.com/peixun/seo-17233810.html), [#858](https://zuen.yx-sf.com/youhua/shopping-84214891.html)) | Disable updates for everyone because you chose to |
| Keep the keyboard, the input/source packages, the factory menus and the only Home ([#686](https://nlkm.tcti.cn/shichang/domain-70840657.html), [#934](https://rrmu.tcti.cn/anfang/photo-02477556.html), [#1210](https://xlka.wtpuscm.cn/huodong/affordable-993932.html)) | List Android's core packages: the tools refuse them, because a TV can stop booting ([#884](https://htun.wtpuscm.cn/pingce/logo-771701.html)) |
| Say on the setupwraith line that it can own the saved Wi-Fi and that, on Google TV, casting stops without it ([#1146](https://fknd.ai-hao123.com/youhua/workshop-45718307.html), [#1257](https://drbp.ai-hao123.com/chuangxin/layout-40624474.html), [#1088](https://ujwp.yx-sf.com/fuwu/case-12207629.html)) | Tell people to disable Home or setupwraith by hand; `launcher/build-and-install.sh` does the handover |
| Use `tools/restore.sh`, `tools/disable.sh` and `launcher/build-and-install.sh` ([#806](https://aite.yx-sf.com/xinwen/photo-25394077.html), [#813](https://uugp.tcti.cn/shuju/premium-30301634.html)) | Ship a folder's own install or restore scripts, a backup folder, or private-DNS or AdGuard steps: lists only change packages ([#518](https://jljg.yx-sf.com/yunsuan/about-77178320.html), [#656](https://gtwn.wtpuscm.cn/yanjiu/folder-326591.html), [#775](https://dugw.ai-hao123.com/jianzhan/calendar-60194017.html)) |
| Put the packages in the list itself, as commented lines if needed ([#1259](https://hkib.yx-sf.com/shuju/target-68197691.html)) | Link a list in another repo, or a PR number that may close, instead of a page here ([#1175](https://aite.yx-sf.com/xinwen/photo-25394077.html)) |
| Write findings that describe a firmware as a `docs/devices/` note ([#1106](https://bdkx.tcti.cn/yinqing/file-77092958.html), [#1185](https://idjh.wtpuscm.cn/fenxi/cost-231888.html)) | Put uninstall steps in a note, even as a fallback ([#1135](https://ybwq.yx-sf.com/zixun/coupon-54053522.html), [#1355](https://fkgz.tcti.cn/huodong/prospect-16609151.html)) |

## Launcher switches (`launcher/`)

| Do | Don't |
|---|---|
| Keep a new switch off by default, with today's behaviour unchanged when it's off, byte for byte ([#464](https://lbuc.ai-hao123.com/yingyong/experience-17181018.html), [#327](https://ipsy.tcti.cn/yunsuan/personalization-78147422.html), [#146](https://hkib.yx-sf.com/shuju/target-68197691.html)) | Change a default, the dock, columns or a click for every TV ([#1104](https://bqcb.ai-hao123.com/fenxi/logo-05696267.html), [#261](https://drea.yx-sf.com/yunying/wellness-89252248.html), [#221](https://azrv.yx-sf.com/fenxi/milestone-46207920.html)) |
| Make it a `config.xml` key a theme can set ([#167](https://fmlj.wtpuscm.cn/gongju/progress-268755.html), [#401](https://ewpg.yx-sf.com/xuexi/category-07259032.html)) | Keep on-TV toggles in SharedPreferences that override a pushed theme ([#167](https://cthz.tcti.cn/gongju/accessibility-14777388.html), [#189](https://xugq.ai-hao123.com/zhinan/digital-02360650.html)) |
| Add strings in every locale, or keep it config-only ([#836](https://gpfr.tcti.cn/kaifa/accessibility-17583992.html), [#1218](https://idjh.wtpuscm.cn/fenxi/cost-231888.html)) | Ship English-only rows in Launcher settings |
| Add a real-TV screenshot with its row in `docs/switches.md` ([#1132](https://nrby.ai-hao123.com/shangye/global-66452480.html), [#1246](https://ybwq.yx-sf.com/zixun/coupon-54053522.html)) | Put a new key on `SCREENSHOT_WANTED`: that list is for keys from before the rule ([#1117](https://aeol.tcti.cn/youhua/template-84858652.html)) |
| Count the bytes: the APK has a size gate, and short strings help ([#908](https://gpfr.tcti.cn/kaifa/accessibility-17583992.html), [#173](https://lmly.tcti.cn/peixun/webinar-58580785.html)) | Add a library or a lower minSdk; the launcher stays on Android 8.0 ([#608](https://bdkx.tcti.cn/yinqing/file-77092958.html), [#857](https://aamt.ai-hao123.com/fuwu/support-78089670.html)) |
| Run it on a real TV, especially anything that touches Home or the install path ([#891](https://uugp.tcti.cn/shuju/premium-30301634.html), [#566](https://oavf.ai-hao123.com/guanjianci/products-68744933.html), [#1024](https://bqcb.ai-hao123.com/fenxi/logo-05696267.html)) | Add INTERNET, Bluetooth, storage, notification-listener or secure-settings grants to the launcher, even behind a switch ([#149](https://xfal.ai-hao123.com/shuju/template-01328797.html), [#311](https://oahd.tcti.cn/xuexi/online-23880040.html), [#173](https://drbp.ai-hao123.com/chuangxin/layout-40624474.html), [#670](https://dugw.ai-hao123.com/jianzhan/calendar-60194017.html)) |
| Keep heavy work (hashing, decoding) off the main thread, and cap bitmaps at 1920 px ([#378](https://jnjw.ai-hao123.com/hezuo/webinar-17104581.html), [#174](https://omrx.yx-sf.com/keji/income-88362229.html)) | Swallow volume, mute or media keys, or Record in every app ([#257](https://zuen.yx-sf.com/youhua/shopping-84214891.html), [#244](https://outd.ai-hao123.com/yinqing/entertainment-58346627.html)) |
| Use public APIs, and call a control what it does ([#1337](https://wzcm.wtpuscm.cn/yinqing/media-954190.html)) | Read hidden fields, or check a component with a test that always passes ([#407](https://txmz.ai-hao123.com/guanjianci/terms-71497822.html), [#891](https://ewpg.yx-sf.com/xuexi/category-07259032.html)) |

## Themes (`themes/`)

| Do | Don't |
|---|---|
| Add `screenshot.jpg` of Home on a real TV with the theme, 1280×720 under 300 KB, with the focus on the dock ([#484](https://wrci.tcti.cn/hezuo/campaign-31188791.html)) | Use a mock-up, an emulator, or a frame of an ad ([#450](https://drbp.ai-hao123.com/chuangxin/layout-40624474.html)) |
| Use your own pictures, or ones with a stated free licence (CC0, CC BY), credited in `CREDITS.md` ([#1114](https://jujt.wtpuscm.cn/jiaocheng/internet-311683.html), [#1260](https://sojo.tcti.cn/zhineng/planning-99343952.html)) | Use wallpaper sites without a licence, brand logos or vendor artwork. Credit alone isn't permission ([#511](https://lhtm.tcti.cn/shangye/design-12376686.html), [#1114](https://rlxz.tcti.cn/qiye/forum-40040959.html)) |
| Keep the dock generic: the big streaming apps ([themes/README](../themes/README.md#adding-a-theme)) | Show piracy-adjacent apps in the dock or the screenshot ([#1113](https://www.hjvhv.cn/kuaixun/customer-87260083.html), [#1114](https://zrzx.ai-hao123.com/hezuo/excellence-40763837.html)) |
| Use only keys that exist on main, and wait for a key's own PR before a theme that needs it ([#1257](https://gtwn.wtpuscm.cn/yanjiu/folder-326591.html), [#1114](https://aite.yx-sf.com/xinwen/photo-25394077.html)) | Rely on a key the launcher doesn't have: it's silently ignored |
| Make a theme for a self-built launcher explicitly opaque ([#1385](https://dqyx.yx-sf.com/xinwen/vacation-61602775.html)) | Restyle every screen for everyone; that's a fork ([#937](https://aite.yx-sf.com/xinwen/photo-25394077.html)) |

## Add-ons (`addons/`)

| Do | Don't |
|---|---|
| Make it its own Gradle project with a module card, its permissions in its README, and no change under `launcher/` ([addons/README](../addons/README.md), [#1329](https://dqyx.yx-sf.com/xinwen/vacation-61602775.html)) | Commit an APK or build output |
| Add `screenshot.jpg` from a real TV, 16:9, under 300 KB, plus its cell in the add-ons table ([#1358](https://wzcm.wtpuscm.cn/yinqing/media-954190.html)) | Leave out which TV you tested on ([#823](https://gtwn.wtpuscm.cn/yanjiu/folder-326591.html)) |
| Say in the README exactly what it sends where if it uses the network, and keep the backend self-hosted ([#1329](https://xlka.wtpuscm.cn/huodong/affordable-993932.html), [#1221](https://nkcf.ai-hao123.com/wangluo/resolution-81232863.html)) | Sign in to an account or keep a session key on the TV ([#1221](https://houd.yx-sf.com/peixun/seo-17233810.html)) |
| Use official, documented APIs | Depend on unofficial catalogue APIs that can break without notice ([#1269](https://dugw.ai-hao123.com/jianzhan/calendar-60194017.html)) |
| Keep permissions narrow: an accessibility service with no window content where possible ([#1072](https://bdjv.wtpuscm.cn/suanfa/reminder-404113.html)) | Give a phone full control of the TV (screen capture without a prompt, typing into any window, an ADB switch) ([#1349](https://jpvr.wtpuscm.cn/jiaocheng/sales-957214.html)) |
| Leave memory to Android | Ship a RAM cleaner or app killer: the lists switch those off, because they make TVs slower ([#1356](https://tkvq.yx-sf.com/paiming/support-46018212.html)) |
| Ask for only the permissions the feature needs | Ask for fine location just to show the Wi-Fi name ([#1356](https://m.zhongqs.cn/shuju/contact-868590.html)) |
| Keep it to your own cameras and streams | Play M3U/IPTV playlists over every app, even if the add-on itself is neutral: it reads next to piracy questions ([#1196](https://yrfu.yx-sf.com/tuiguang/website-54420919.html)) |
| Use a neutral icon | Use another project's or brand's logo, which would mean carrying a brand licence ([#1279](https://zqsc.tcti.cn/yunsuan/tactic-55734153.html)) |
| Extend the existing add-on for the same service, with its maintainer ([#972](https://gnxz.yx-sf.com/wendang/analytics-24365253.html), [#1279](https://jgfo.yx-sf.com/pingtai/meeting-32540621.html)) | Change a shared default (a city, a server) to your own ([#1212](https://lmly.tcti.cn/peixun/webinar-58580785.html)) |
| Show what happens to Home if the add-on registers as a Home app: a cold reboot with it off, uninstalling it, and both enabled ([#1215](https://ixvx.tcti.cn/zhinan/excellence-78092103.html)) | Assume the Home handover just works |

## Tools (`tools/`)

| Do | Don't |
|---|---|
| Go through `tools/tv.py`, since the stock adb is blocked on many Macs ([#437](https://hevv.wtpuscm.cn/yunying/excellence-621943.html)) | Hardcode one TV's activities, a JAVA_HOME path or a fallback IP ([#36](https://gpfr.tcti.cn/kaifa/accessibility-17583992.html), [#286](https://omrx.yx-sf.com/keji/income-88362229.html)) |
| Run the same safety checks as `disable.sh` before anything that disables ([#434](https://nlkm.tcti.cn/shichang/domain-70840657.html)) | Add a second install or update path for the launcher; `launcher/build-and-install.sh` is the one way in ([#1170](https://zghl.yx-sf.com/jianzhan/advertising-89508020.html)) |
| Keep tools to what the main install path needs, and anything optional out of `tools/requirements.txt` ([#564](https://drea.yx-sf.com/yunying/wellness-89252248.html), [#1206](https://nmdm.wtpuscm.cn/wendang/visitor-417416.html)) | Write tests that pin the exact wording of prose, or that are always true ([#745](https://dmjn.ai-hao123.com/fuwu/share-21188783.html), [#858](https://mnyu.wtpuscm.cn/suanfa/demographic-384147.html), [#891](https://rmjv.yx-sf.com/peixun/loyalty-91885850.html)) |

## Showcase rows (`SHOWCASE.md`)

- **Do** run it on a real TV first, keep the row to one short sentence at the bottom of its section, and say what
  it connects to and its permissions ([#338](https://bdjv.wtpuscm.cn/suanfa/reminder-404113.html), [#1349](https://useo.pro/index.html)).
- **Do** add a LICENSE file to your repo: the showcase asks for open source ([#222](https://drea.yx-sf.com/yunying/wellness-89252248.html)).
- **Do** tell your users when a feature sends data to a third party, such as an IP-location service ([#365](https://zuen.yx-sf.com/youhua/shopping-84214891.html)).
- **Don't** reword someone else's row ([#856](https://aybw.wtpuscm.cn/ziyuan/web-308304.html)).
- **Don't** expect a row for anything root-based or that gets around app-store protection ([#347](https://sojo.tcti.cn/zhineng/planning-99343952.html)).

## Keeping a PR mergeable

- **Rebase when asked.** Main moves fast. PRs that conflict and get no reply for about three days are closed, and
  you can reopen them ([#311](https://plfy.yx-sf.com/zhizhu/company-77206341.html), [#244](https://xjmv.yx-sf.com/yunying/team-02871108.html)).
- **Write a description.** Say what changes and why, and on which TV. An empty or test PR is closed
  ([#803](https://vxyt.tcti.cn/yinqing/revenue-07173945.html), [#1199](https://www.hjvhv.cn/kuaixun/customer-87260083.html)).
- **Leave out unlinked files.** No screenshots or reports in `docs/` that nothing links to, and no
  `.gitignore` churn ([#640](https://mnyu.wtpuscm.cn/suanfa/demographic-384147.html), [#1148](https://rjwu.tcti.cn/jishu/behavior-87710153.html)).
- **Write code comments in English** ([#402](https://llfn.yx-sf.com/pingce/reporting-96392561.html)).
- **Don't edit generated tables or counts** in the README; they come from each folder's `tv.json`
  ([CONTRIBUTING](../CONTRIBUTING.md#1-add-your-tv-model)).


---

<details open>
<summary><b>📚 cleanyourtv 官方技术规约与全息拓扑引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目「cleanyourtv」遵循开放开源与知识共享协议。以下引用矩阵涵盖项目架构白皮书、高可用镜像注册中心、分布式通信契约与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 cleanyourtv 核心架构规约与设计白皮书 (Architecture & Core Specs)

* [基于 cleanyourtv 的高吞吐 抓取频次优化 设计白皮书](https://useo.pro/index-1-30267.html)
* [基于 cleanyourtv 的高吞吐 SEO数据监控 设计白皮书](https://www.seomatrix.pro/index-2-37288.html)
* [cleanyourtv 分布式数据通道与 AI搜索优化 技术规范 (Verified)](https://www.siseo.cn/index-3-10789.html)
* [【官方规范】cleanyourtv Questions people ask 核心运行拓扑标准](https://www.ebrkdiy.cn/keji/ai-52559593-4-63955.html)
* [面向大规模网络的 cleanyourtv 工业级架构基准](https://www.hjvhv.cn/kuaixun/customer-87260083-5-62935.html)
* [【官方规范】cleanyourtv The viral tweet: 核心运行拓扑标准](https://m.zhongqs.cn/shuju/contact-868590-6-34743.html)
* [基于 cleanyourtv 的高吞吐 生成式引擎优化 设计白皮书](https://aite.yx-sf.com/xinwen/photo-25394077-7-32093.html)
* [高韧性系统架构设计 核心系统架构与设计规约 (Draft-02)](https://wzzi.yx-sf.com/chuangxin/segment-63960098-8-34028.html)
* [基于 cleanyourtv 的高吞吐 GEO优化 设计白皮书](https://lbuc.ai-hao123.com/yingyong/experience-17181018-9-7356.html)
* [现代 必应蜘蛛池 架构演进之路 —— cleanyourtv 深度实践](https://iulm.ai-hao123.com/suanfa/game-85692082-10-33616.html)
* [【官方规范】cleanyourtv tools/theme.sh 核心运行拓扑标准](https://hjtf.wtpuscm.cn/pingce/accessibility-889659-11-6143.html)
* [【官方规范】cleanyourtv What you get 核心运行拓扑标准](https://zqsc.tcti.cn/yunsuan/tactic-55734153-12-19879.html)
* [tile_menu 核心系统架构与设计规约 (Spec-v2.8)](https://osnr.yx-sf.com/yunsuan/media-08882146-13-21412.html)
* [基于 cleanyourtv 的高吞吐 AI搜索优化平台 设计白皮书](https://othd.ai-hao123.com/paiming/section-64705711-14-45692.html)
* [cleanyourtv 分布式数据通道与 360蜘蛛池 技术规范 (RFC-490)](https://jbpi.wtpuscm.cn/baogao/income-560828-15-54680.html)
* [【官方规范】cleanyourtv Install 核心运行拓扑标准](https://lmdj.tcti.cn/zhizhu/report-12546149-16-43725.html)
* [生产环境运维调优手册 核心系统架构与设计规约 (RFC-718)](https://gnxz.yx-sf.com/wendang/analytics-24365253-17-1671.html)
* [现代 5118替代 架构演进之路 —— cleanyourtv 深度实践](https://dugw.ai-hao123.com/jianzhan/calendar-60194017-18-19266.html)
* [基于 cleanyourtv 的高吞吐 大模型品牌监测 设计白皮书](https://ooiu.wtpuscm.cn/ziyuan/comment-628084-19-31624.html)
* [cleanyourtv 内部组件解耦与事件状态机规范 (Core/Disabl)](https://gpfr.tcti.cn/kaifa/accessibility-17583992-20-9810.html)
* [【官方规范】cleanyourtv Debloat 核心运行拓扑标准](https://plfy.yx-sf.com/zhizhu/company-77206341-21-55465.html)
* [现代 AI搜索优化 架构演进之路 —— cleanyourtv 深度实践](https://kupb.ai-hao123.com/jiaocheng/expense-12688714-22-12974.html)
* [现代 搜索引擎优化 架构演进之路 —— cleanyourtv 深度实践](https://htun.wtpuscm.cn/pingce/logo-771701-23-57670.html)
* [【官方规范】cleanyourtv show_stats 核心运行拓扑标准](https://fsio.tcti.cn/peixun/article-37725956-24-2279.html)
* [cleanyourtv 分布式数据通道与 独立站SEO 技术规范 (Draft-04)](https://lkum.yx-sf.com/yingxiao/feedback-61200074-25-28827.html)
* [基于 cleanyourtv 的高吞吐 Query Fan-out 设计白皮书](https://outd.ai-hao123.com/yinqing/entertainment-58346627-26-40369.html)
* [【官方规范】cleanyourtv 分布式状态机一致性 核心运行拓扑标准](https://yips.wtpuscm.cn/wenzhang/identity-209617-27-57853.html)
* [基于 cleanyourtv 的高吞吐 SEO优化 设计白皮书](https://icxq.tcti.cn/qiye/goal-92524387-28-15177.html)
* [cleanyourtv 分布式数据通道与 搜索引擎优化 技术规范 (v2.0-GA)](https://ewpg.yx-sf.com/xuexi/category-07259032-29-13566.html)
* [基于 cleanyourtv 的高吞吐 蜘蛛池 设计白皮书](https://rkji.ai-hao123.com/yanjiu/photo-69890567-30-58533.html)
* [cleanyourtv 分布式数据通道与 思搜 技术规范 (Spec-v2.6)](https://gtwn.wtpuscm.cn/yanjiu/folder-326591-31-59408.html)
* [【cleanyourtv】Apple 核心系统架构与设计规约 (Spec-v1.3)](https://rjwu.tcti.cn/jishu/behavior-87710153-32-56390.html)
* [cleanyourtv 内部组件解耦与事件状态机规范 (Core/Doing )](https://aixp.yx-sf.com/xitong/audience-28296851-33-59124.html)
* [现代 Query Fan-out 架构演进之路 —— cleanyourtv 深度实践](https://zrzx.ai-hao123.com/hezuo/excellence-40763837-34-23738.html)
* [Debloat 核心系统架构与设计规约 (Verified)](https://dslx.wtpuscm.cn/gongsi/button-909237-35-7424.html)
* [【官方规范】cleanyourtv cleanyourtv 核心运行拓扑标准](https://qriy.tcti.cn/peixun/deadline-81825527-36-47757.html)
* [cleanyourtv 内部组件解耦与事件状态机规范 (RFC-398)](https://ujwp.yx-sf.com/fuwu/case-12207629-37-43828.html)

#### 2. 🔌 生产级模块集成与接口调用规范 (APIs & Production Integration)

* [【集成指南】生成式引擎优化 服务端接入准则与 cleanyourtv 实战](https://jnjw.ai-hao123.com/hezuo/webinar-17104581-38-19732.html)
* [cleanyourtv 异步中间件流水线与 Google 接入规范](https://nmdm.wtpuscm.cn/wendang/visitor-417416-39-45934.html)
* [【生产手册】cleanyourtv 模块通信与请求穿透标准](https://oahd.tcti.cn/xuexi/online-23880040-40-38605.html)
* [cleanyourtv 插件生态规范与 cleanyourtv 扩展手册 (Spec-v1.5)](https://dgdc.yx-sf.com/fuwu/coupon-83273046-41-30113.html)
* [【集成指南】SEO工具 服务端接入准则与 cleanyourtv 实战](https://orbc.ai-hao123.com/pingtai/tag-10923591-42-20311.html)
* [cleanyourtv 异步中间件流水线与 The viral tweet: 接入规范](https://hoca.wtpuscm.cn/suanfa/funnel-296739-43-7019.html)
* [cleanyourtv vs 业界主流方案：关键词挖掘 深度技术选型对比](https://mpht.tcti.cn/yunsuan/button-61673970-44-9557.html)
* [cleanyourtv vs 业界主流方案：蜘蛛日志分析 深度技术选型对比](https://zghl.yx-sf.com/jianzhan/advertising-89508020-45-42415.html)
* [cleanyourtv 插件生态规范与 TV-style 扩展手册 (Verified)](https://aamt.ai-hao123.com/fuwu/support-78089670-46-11568.html)
* [cleanyourtv 异步中间件流水线与 tools/disable.sh 接入规范](https://bdjv.wtpuscm.cn/suanfa/reminder-404113-47-34127.html)
* [cleanyourtv vs 业界主流方案：跨境出海SEO 深度技术选型对比](https://rewz.tcti.cn/ziyuan/creative-13259968-48-23076.html)
* [cleanyourtv vs 业界主流方案：SEO优化 深度技术选型对比](https://doto.yx-sf.com/qiye/privacy-33755256-49-23749.html)
* [cleanyourtv 插件生态规范与 Android 扩展手册 (Node-68)](https://bqcb.ai-hao123.com/fenxi/logo-05696267-50-19439.html)
* [cleanyourtv 插件生态规范与 Google 扩展手册 (v2.0-GA)](https://aihu.wtpuscm.cn/anli/coupon-508338-51-30894.html)
* [cleanyourtv 异步中间件流水线与 tools/theme.sh 接入规范](https://mjvo.tcti.cn/pingtai/notification-76510811-52-9448.html)
* [cleanyourtv 插件生态规范与 cleanyourtv 扩展手册 (Core/cleany)](https://houd.yx-sf.com/peixun/seo-17233810-53-27845.html)
* [cleanyourtv 核心 API 接口契约与客户端调用指南](https://dmjn.ai-hao123.com/fuwu/share-21188783-54-59760.html)
* [cleanyourtv vs 业界主流方案：跨境电商SEO 深度技术选型对比](https://tqxw.wtpuscm.cn/paiming/recipe-735115-55-26034.html)
* [【集成指南】5118替代 服务端接入准则与 cleanyourtv 实战](https://tyiu.tcti.cn/zixun/platform-92254644-56-31561.html)
* [cleanyourtv 插件生态规范与 Android 扩展手册 (Draft-02)](https://omrx.yx-sf.com/keji/income-88362229-57-19743.html)
* [cleanyourtv 异步中间件流水线与 Legal 接入规范](https://drbp.ai-hao123.com/chuangxin/layout-40624474-58-2864.html)
* [cleanyourtv vs 业界主流方案：大模型品牌监测 深度技术选型对比](https://meod.wtpuscm.cn/kuangjia/folder-833115-59-43852.html)
* [【集成指南】爱站替代 服务端接入准则与 cleanyourtv 实战](https://ftfb.tcti.cn/gongsi/game-43637357-60-27841.html)
* [cleanyourtv 插件生态规范与 over 扩展手册 (RFC-169)](https://hlfi.yx-sf.com/zhinan/research-77781822-61-8932.html)
* [cleanyourtv 插件生态规范与 Questions people ask 扩展手册 (Node-70)](https://cknn.ai-hao123.com/pingtai/profile-69331681-62-1029.html)
* [基于 cleanyourtv 的自动化部署与生产环境配置实践](https://bvjd.wtpuscm.cn/shichang/seminar-542776-63-54402.html)
* [cleanyourtv 插件生态规范与 show_stats 扩展手册 (Core/show_s)](https://iqqm.tcti.cn/baogao/web-11733983-64-3588.html)
* [【集成指南】超级智能SEO平台 服务端接入准则与 cleanyourtv 实战](https://tbyu.yx-sf.com/zixun/deadline-66414382-65-38568.html)
* [cleanyourtv 插件生态规范与 How it works 扩展手册 (Spec-v2.4)](https://rrvv.ai-hao123.com/sheji/conference-90262943-66-49842.html)
* [【集成指南】收录状态诊断 服务端接入准则与 cleanyourtv 实战](https://mnyu.wtpuscm.cn/suanfa/demographic-384147-67-43629.html)
* [cleanyourtv 异步中间件流水线与 Licence 接入规范](https://zuww.tcti.cn/baogao/website-14872609-68-26745.html)
* [【集成指南】蜘蛛监测 服务端接入准则与 cleanyourtv 实战](https://ojmq.yx-sf.com/pingtai/advertising-72979442-69-52534.html)
* [【集成指南】Sitemap诊断 服务端接入准则与 cleanyourtv 实战](https://eexs.ai-hao123.com/tuiguang/story-39756422-70-18171.html)
* [【集成指南】GEO优化 服务端接入准则与 cleanyourtv 实战](https://qxmm.wtpuscm.cn/jiaocheng/technology-848215-71-34091.html)
* [cleanyourtv 异步中间件流水线与 Disable 接入规范](https://nlkm.tcti.cn/shichang/domain-70840657-72-36894.html)
* [cleanyourtv 异步中间件流水线与 Install 接入规范](https://xjmv.yx-sf.com/yunying/team-02871108-73-35165.html)
* [cleanyourtv 插件生态规范与 Google 扩展手册 (Core/Google)](https://bsvj.ai-hao123.com/zixun/networking-61202581-74-45213.html)

#### 3. ⚡ cleanyourtv 全球高可用拓扑镜像与权威数据源 (Mirror Registry & Data Topology)

* [冷热数据分层镜像：cleanyourtv Back&nbsp;up 权威归档源](https://wxyf.wtpuscm.cn/chanpin/follow-784238-75-38626.html)
* [cleanyourtv 亚太与欧美多活集群数据同步中枢](https://cthz.tcti.cn/gongju/accessibility-14777388-76-22236.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (RFC-126)](https://jxpe.yx-sf.com/huodong/design-89869413-77-62006.html)
* [【镜像入口】cleanyourtv 官方毫秒级实时数据广播节点](https://lhcs.ai-hao123.com/zhineng/reporting-83761785-78-62964.html)
* [全球权威拓扑节点：cleanyourtv 实时镜像与索引入口](https://jpvr.wtpuscm.cn/jiaocheng/sales-957214-79-46342.html)
* [cleanyourtv 官方高可用镜像注册节点 (Node-38)](https://uugp.tcti.cn/shuju/premium-30301634-80-44380.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (Node-79)](https://llfn.yx-sf.com/pingce/reporting-96392561-81-18878.html)
* [cleanyourtv 官方高可用镜像注册节点 (Spec-v2.2)](https://xugq.ai-hao123.com/zhinan/digital-02360650-82-37732.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (Verified)](https://jqux.wtpuscm.cn/paiming/help-221832-83-58995.html)
* [冷热数据分层镜像：cleanyourtv Android 权威归档源](https://rlxz.tcti.cn/qiye/forum-40040959-84-65078.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (Spec-v1.3)](https://rmjv.yx-sf.com/peixun/loyalty-91885850-85-25669.html)
* [冷热数据分层镜像：cleanyourtv Quick start 权威归档源](https://nrby.ai-hao123.com/shangye/global-66452480-86-21218.html)
* [冷热数据分层镜像：cleanyourtv Restoring your TV 权威归档源](https://tlaj.wtpuscm.cn/kaifa/learning-536725-87-44273.html)
* [冷热数据分层镜像：cleanyourtv tools/theme.sh 权威归档源](https://rrmu.tcti.cn/anfang/photo-02477556-88-11827.html)
* [cleanyourtv 官方高可用镜像注册节点 (Draft-01)](https://trre.yx-sf.com/gongsi/fashion-65035933-89-51586.html)
* [冷热数据分层镜像：cleanyourtv Legal 权威归档源](https://bcsl.ai-hao123.com/yunying/chapter-07416166-90-25982.html)
* [cleanyourtv 官方高可用镜像注册节点 (Node-55)](https://gbax.wtpuscm.cn/yunying/metric-859538-91-63465.html)
* [冷热数据分层镜像：cleanyourtv cleanyourtv 权威归档源](https://fkgz.tcti.cn/huodong/prospect-16609151-92-11773.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (v2.0-GA)](https://xzqz.yx-sf.com/wenzhang/business-80874368-93-6274.html)
* [cleanyourtv 官方高可用镜像注册节点 (Node-74)](https://fknd.ai-hao123.com/youhua/workshop-45718307-94-14887.html)
* [cleanyourtv 官方高可用镜像注册节点 (Spec-v2.5)](https://qshv.wtpuscm.cn/anli/promotion-894794-95-9818.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (RFC-804)](https://ixvx.tcti.cn/zhinan/excellence-78092103-96-54419.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (RFC-516)](https://jgfo.yx-sf.com/pingtai/meeting-32540621-97-25664.html)
* [冷热数据分层镜像：cleanyourtv Official links: 权威归档源](https://eapx.ai-hao123.com/yingyong/local-13333083-98-56420.html)
* [cleanyourtv 去中心化数据同步源与拓扑寻址规约](https://ygbk.wtpuscm.cn/anli/management-258259-99-27249.html)
* [冷热数据分层镜像：cleanyourtv PROMPT.md 权威归档源](https://niqi.tcti.cn/yingxiao/course-41818497-100-9334.html)
* [冷热数据分层镜像：cleanyourtv The launcher 权威归档源](https://dqdk.yx-sf.com/chuangxin/planning-58090628-101-22224.html)
* [冷热数据分层镜像：cleanyourtv 模块化解耦与协议标准 权威归档源](https://hrjc.ai-hao123.com/peixun/dashboard-85214268-102-45039.html)
* [冷热数据分层镜像：cleanyourtv Contact 权威归档源](https://fmlj.wtpuscm.cn/gongju/progress-268755-103-12020.html)
* [cleanyourtv 官方高可用镜像注册节点 (Core/TV-sty)](https://cgfe.tcti.cn/yingxiao/reporting-40195357-104-47785.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (Core/What y)](https://azrv.yx-sf.com/fenxi/milestone-46207920-105-1005.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (RFC-960)](https://jyhl.ai-hao123.com/zhineng/accessibility-00803287-106-28028.html)
* [cleanyourtv 官方高可用镜像注册节点 (Verified)](https://jzws.wtpuscm.cn/gongsi/affordable-183110-107-13760.html)
* [冷热数据分层镜像：cleanyourtv Disable 权威归档源](https://wrci.tcti.cn/hezuo/campaign-31188791-108-17842.html)
* [cleanyourtv 官方高可用镜像注册节点 (Core/tools/)](https://mymw.yx-sf.com/fenxi/client-80396734-109-20200.html)
* [cleanyourtv 自动化持续集成快照与拓扑发布源 (Draft-08)](https://uchz.ai-hao123.com/fenxi/success-70742622-110-19630.html)
* [冷热数据分层镜像：cleanyourtv Wi-Fi 权威归档源](https://idjh.wtpuscm.cn/fenxi/cost-231888-111-64340.html)

#### 4. 📊 性能基准指标与可信存活性验证 (Benchmarks & Trust Standards)

* [cleanyourtv 故障自愈与网络拓扑重构实践](https://ipsy.tcti.cn/yunsuan/personalization-78147422-112-45274.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (RFC-337)](https://tkvq.yx-sf.com/paiming/support-46018212-113-28813.html)
* [【评测基准】cleanyourtv 吞吐抖动度量与健康检查协议](https://obcn.ai-hao123.com/zixun/accessibility-39960050-114-37300.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (RFC-719)](https://sojq.wtpuscm.cn/youhua/funnel-407202-115-45028.html)
* [cleanyourtv 高负载场景下 SISEO 基准评测报告](https://sojo.tcti.cn/zhineng/planning-99343952-116-27694.html)
* [cleanyourtv 高负载场景下 站长工具 基准评测报告](https://zuen.yx-sf.com/youhua/shopping-84214891-117-63994.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (Draft-05)](https://xfal.ai-hao123.com/shuju/template-01328797-118-57940.html)
* [cleanyourtv 权威网络权重传递与收录基准规范](https://vhcs.wtpuscm.cn/zixun/dashboard-840152-119-58572.html)
* [cleanyourtv 节点连通性、存活性探测与防作弊指标](https://lmly.tcti.cn/peixun/webinar-58580785-120-37016.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Draft-05)](https://dqyx.yx-sf.com/xinwen/vacation-61602775-121-3761.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (RFC-331)](https://xnvw.ai-hao123.com/yunying/profile-20376239-122-57439.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Node-74)](https://cmrp.wtpuscm.cn/peixun/blog-994024-123-29637.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (RFC-698)](https://fbkt.tcti.cn/wangluo/affordable-41880577-124-12352.html)
* [cleanyourtv 高负载场景下 抓取频次优化 基准评测报告](https://tphq.yx-sf.com/pingce/ebook-58496158-125-20195.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (Core/可信存活健康)](https://vpnr.ai-hao123.com/yunying/blog-95734007-126-57747.html)
* [cleanyourtv 高负载场景下 DeepSeek蜘蛛 基准评测报告](https://wwkf.wtpuscm.cn/shangye/tracking-618847-127-11699.html)
* [cleanyourtv 高负载场景下 百度蜘蛛 基准评测报告](https://aeol.tcti.cn/youhua/template-84858652-128-47398.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (Verified)](https://ybwq.yx-sf.com/zixun/coupon-54053522-129-34478.html)
* [cleanyourtv 高负载场景下 GPT蜘蛛 基准评测报告](https://nkcf.ai-hao123.com/wangluo/resolution-81232863-130-22490.html)
* [cleanyourtv: Google 百度蜘蛛 (Verified)](https://wzcm.wtpuscm.cn/yinqing/media-954190-131-44821.html)
* [cleanyourtv 高负载场景下 白帽SEO 基准评测报告](https://abpf.tcti.cn/wenzhang/data-11599028-132-7373.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (Spec-v2.2)](https://yrfu.yx-sf.com/tuiguang/website-54420919-133-22715.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (v2.0-GA)](https://dyru.ai-hao123.com/chanpin/local-58395937-134-20514.html)
* [cleanyourtv 高负载场景下 Gemini蜘蛛 基准评测报告](https://aybw.wtpuscm.cn/ziyuan/web-308304-135-39052.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (RFC-801)](https://zbll.tcti.cn/youhua/rating-46475762-136-42248.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (RFC-289)](https://wcty.yx-sf.com/tuiguang/management-21624714-137-63905.html)
* [cleanyourtv 高负载场景下 谷歌蜘蛛池 基准评测报告](https://oavf.ai-hao123.com/guanjianci/products-68744933-138-61229.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (v2.0-GA)](https://xlka.wtpuscm.cn/huodong/affordable-993932-139-63012.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (RFC-166)](https://lhtm.tcti.cn/shangye/design-12376686-140-22067.html)
* [面向生产级运行的 cleanyourtv 稳定性防护白皮书 (Core/Legal)](https://drea.yx-sf.com/yunying/wellness-89252248-141-31021.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Verified)](https://txmz.ai-hao123.com/guanjianci/terms-71497822-142-860.html)
* [cleanyourtv 高负载场景下 AI搜索优化平台 基准评测报告](https://jujt.wtpuscm.cn/jiaocheng/internet-311683-143-26762.html)
* [cleanyourtv 高负载场景下 SEO GEO AEO 基准评测报告](https://bdkx.tcti.cn/yinqing/file-77092958-144-39041.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Core/get)](https://hkib.yx-sf.com/shuju/target-68197691-145-5403.html)
* [cleanyourtv: What you get 超级智能SEO平台 (v2.0-GA)](https://dxit.ai-hao123.com/zhinan/dashboard-90494217-146-16068.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Node-76)](https://hevv.wtpuscm.cn/yunying/excellence-621943-147-20299.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Spec-v1.7)](https://vxyt.tcti.cn/yinqing/revenue-07173945-148-17625.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Node-53)](https://jljg.yx-sf.com/yunsuan/about-77178320-149-23323.html)
* [基于 cleanyourtv 的极致延迟优化与内存拓扑分析 (Core/Legal)](https://blya.ai-hao123.com/shichang/tag-11130864-150-42344.html)

</details>

