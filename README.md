#=============UserScript=============#
# 项目名称：App解锁合集
# 项目作者：chxm1023
# 📢 频道：https://t.me/chxm1023
# 👥 群组：https://t.me/chxm1023_Chat

#============【使用说明】==============#
# 使用声明：作者并未参与任何形式的金钱交易，仅限测试和学习，请勿转载与贩卖，下载使用后24小时请删除⚠️⚠️⚠️⚠️⚠️

# 使用方法：先开脚本再打开App，自动会生效，如果无效就关了重开或者按一下恢复购买，在还不行就卸载App重新安装！最后还不行的话就是脚本失效了！

# 更新日期：2023-11-11

# 项目解锁App下载地址：https://too.st/chxm1023

#=============UserScript=============#

# Revenuecat解锁系列
# hostname = api.revenuecat.com
^https?:\/\/api\.revenuecat\.com\/.+\/(receipts$|subscribers\/?(.*?)*$) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Reheji.js
^https?:\/\/api\.revenuecat\.com\/.+\/(receipts$|subscribers\/?(.*?)*$) url script-request-header https://raw.githubusercontent.com/chxm1023/Rewrite/main/Reheji.js

#************************************#
# iTunes解锁系列
# hostname = buy.itunes.apple.com
^https?:\/\/buy\.itunes\.apple\.com\/verifyReceipt$ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/iTunes.js

#************************************#
# Nicegram
# hostname = restore-access.indream.app
#^https?:\/\/restore-access\.indream\.app\/restoreAccess\?id=\d{5,10} url echo-response text/json echo-response https://raw.githubusercontent.com/chxm1023/Rewrite/main/Nicegram.js
# 第二个脚本，二选一即可
^https?:\/\/restore-access\.indream\.app\/restoreAccess url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/nicegram.js

#************************************#
# 绘影字幕
# hostname = api.bluepulse.cn
^https?:\/\/api\.bluepulse\.cn\/bluepulse-caption-server-front\/api\/.+\/user\/app-vip-info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/hyzm.js

#************************************#
# 搜图神器
# hostname = wallpaper.soutushenqi.com
^http:\/\/wallpaper\.soutushenqi\.com\/api\/.+\/account\/token url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/soutu.js

#************************************#
# PS 图片编辑
# hostname = lcs-mobile-cops.adobe.io
^https?:\/\/lcs-mobile-cops\.adobe\.io\/mobile_profile url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Ps.js

#************************************#
# 彩云天气
# hostname = *.cyapi.cn, *.caiyunapp.com, adx.sogaha.cn
^https?:\/\/(biz|wrapper|starplucker)\.(cyapi|caiyunapp)\.(cn|com)\/(.+\/(user\?app_name|activity\?app_name|visitors|operation\/banners)|p\/v\d\/(vip_info|user_info)) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/caiyuntianqi.js
^https?:\/\/(api|wrapper)\.(cyapi|caiyunapp)\.(cn|com)\/v\d\/(satellite|nafp\/origin_images) url script-request-header https://raw.githubusercontent.com/chxm1023/Rewrite/main/caiyuntianqi.js
# 以下新版已失效
#https?:\/\/biz\.caiyunapp\.com\/(membership_rights|v2\/user) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/caiyun_svip.js
^https?:\/\/ad\.(caiyunapp|cyapi)\.(cn|com) url reject-200
^http:\/\/adx\.sogaha\.cn\/sdk\/ad\/get url reject-200

#************************************#
# 一言
# hostname = app.yiyan.art
^https?:\/\/app\.yiyan\.art\/yiyan url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yiyan.js

#************************************#
# 网速管家
# hostname = api*.speedtest.cn
^https?:\/\/api.*\.speedtest\.cn\/user\/info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/wsgj.js

#************************************#
# 悟饭掌悦
# hostname = iosv2.cjapi.5fun.com
http:\/\/iosv2\.cjapi\.5fun\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/wfzy.js

#************************************#
# 酷我音乐
# hostname = *.kuwo.cn, *.kwcdn.kuwo.cn, *.lrts.me
# 酷我音乐_AdBlock
^https?:\/\/rich\.kuwo\.cn\/AdService\/kaiping\/.+ url reject
# 酷我音乐_AdBlock
^https?:\/\/.+\.kwcdn\.kuwo\.cn\/star\/upload\/.+ url reject
# 酷我音乐_AdBlock
^https?:\/\/mobilead\.kuwo\.cn\/EcomResourceServer\/Ad url reject
# 酷我听书_Blockad
https?:\/\/audiobookpay\.kuwo\.cn/a\.p\?op=get_advertright url reject-dict
# 酷我听书_Blockad
https?:\/\/omp-audiobookpay\.lrts\.me\/a\.p\?op=get_advertright url reject-dict
# 酷我音乐_添加已购音乐
^https?:\/\/musicpay\.kuwo\.cn\/music\.pay\?uid\=\d+ url 302 http://musicpay.kuwo.cn/music.pay?uid=2
# 酷我音乐_会员(已失效)
#^https?:\/\/.*\.(kuwo|lrts)\.(cn|me)\/(a\.p|music\.pay|(vip\/(v2|enc)\/(theme|user\/vip))|(EcomResource|(Mobile)?Ad)Serv(er|ice)).* url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/kwyy.js

#************************************#
# Emby(解锁播放权限)
# hostname = mb3admin.com
^https?:\/\/mb3admin\.com\/admin\/service(\/registration\/validateDevice|\/appstore\/register|\/registration\/validate|\/registration\/getStatus|\/supporter\/retrievekey) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/embycrack.js

#************************************#
# 扫描全能王
# hostname = *.camscanner.com, *.intsig.net
^https?:\/\/.*\.(intsig\.net|camscanner\.com) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/CamScanner.js

#************************************#
# 百度网盘，一刻相册 解锁部分功能
# hostname = pan.baidu.com
^https?:\/\/pan\.baidu\.com\/(youai\/(user\/.+\/getminfo|membership\/.+\/adswitch)|(rest\/.+\/membership\/user|act\/.+\/(bchannel|welfare)\/list|api\/usercfg)) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/bdcloud.js

#************************************#
# 阿里云盘 净化/解锁SVIP
# hostname = *.aliyundrive.com, *.alipan.com
^https?:\/\/(api|member)\.(aliyundrive|alipan)\.com\/(.+\/(users|activity|user\/get)|((business|apps)\/.+\/users|adrive\/.+\/user)) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/alidrive.js

#************************************#
# Picsart美易_图片视频编辑器
# hostname = api.meiease.cn
^https?:\/\/api\.meiease\.cn\/shop\/subscription\/(validate|apple\/purchases) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/picsart.js

#************************************#
# 起伏
# hostname = api.risingfalling.com
https?:\/\/api\.risingfalling\.com\/api\/vip\/detail url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/qifu.js

#************************************#
# 布丁锁屏
# hostname = screen-lock.*.com
^https?:\/\/screen-lock\.(sm-check|51wnl-cq)\.com\/userApi\/saveUser.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/bdsp.js

#************************************#
# Wallcraft-动态壁纸
# hostname = *.wallpaperscraft.com
^https?:\/\/billing-ios\.wallpaperscraft\.com\/verify_receipt\/remove_ads$ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Wall.js

#************************************#
# Symbolab(需要登录)
# hostname = scibug.com
^https?:\/\/scibug\.com\/appleSubscriptionValidate$ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Syjsq.js

#************************************#
# Spotify (不能超高音质)
# hostname = spclient.wg.spotify.com
^https?:\/\/spclient\.wg\.spotify\.com\/(bootstrap\/v1\/bootstrap|user-customization-service\/v1\/customize)$ url script-response-body https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-proto.js
^https?:\/\/spclient\.wg\.spotify\.com\/(artistview\/v1\/artist|album-entity-view\/v2\/album)\/ url script-request-header https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-json.js

#************************************#
# 堆糖
# hostname = *.duitang.com
^http[s]?:\/\/.*\.duitang\.com\/napi url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/duitang.js

#************************************#
# Boom
# hostname = apimboom2.globaldelight.net
^https?:\/\/apimboom2\.globaldelight\.net\/itunesreceipt_v2\.php$ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/boom.js

#************************************#
# 傲软抠图，傲软扫描，傲软PDF转换，傲软PDF编辑，傲软投屏，咖映，轻闪PDF，乃糖小组件，佐糖，佐糖照片修复
# hostname = *.aoscdn.com, *.apsapp.cn
^https?:\/\/.*\.(aoscdn\.com|apsapp\.cn) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/arqjt.js

#************************************#
# Agenda
# hostname = accounts.agenda.com
^https?:\/\/accounts\.agenda\.com\/users\/.*\/license url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Ag.js

#************************************#
# 云听-全国电台/有声听书
# hostname = *.radio.cn, 60.205.171.165
(^https?:\/\/(ytmsout|ytapi)\.radio\.cn|60\.205\.171\.165)\/(contentBiz|publish|rights|user\/appUser\/getUserInfo|ytsrv\/srv\/appUser\/getUserInfoH5) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yunting.js
# 去除开屏广告/浮窗
^https?:\/\/ytmsout\.radio\.cn\/publish\/recScreen\/getLoadPage url reject-200

#************************************#
# Cubox-收藏阅读
# hostname = cubox.*
^https?:\/\/cubox\.(pro|cc)\/.+\/api\/userInfo url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Cb.js

#************************************#
# 小组件盒子
# hostname = widget-box-api.codefuture.top
^https?:\/\/widget-box-api\.codefuture\.top\/.+\/users\/me url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/xzjhz.js

#************************************#
# 格式转换
# hostname = format-api.netpock.com
http:\/\/format-api\.netpock\.com\/api\/user_info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/gszh.js

#************************************#
# 手机扫描，图片编辑，九宫格切图，头像制作，早安打卡，配音
# hostname = *.dicallapp.com
http:\/\/.*\.dicallapp\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/zhfqjt.js

#************************************#
# 如期
# hostname = www.freshhome.top
^https?:\/\/www\.freshhome\.top url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/rq.js

#************************************#
# iLove PDF
# hostname = service.ilovepdf.com
^https?:\/\/service\.ilovepdf\.com\/.+\/user url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/ilove.js

#************************************#
# VN-视频剪辑
# hostname = api2.vlognow.me
^https?:\/\/api2\.vlognow\.me\/vn-pay\/api\/.+\/public\/iap\/receipt\/status?(.*?)*$ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/vn.js

#************************************#
# 日杂相机，fomz相机
# hostname = *.imendon.com
^https?:\/\/.*\.imendon\.com\/.+\/purchase\/vip\/verification url response-body "isValid":\d response-body "isValid":1

#************************************#
# 大神水印
# hostname = dashen-api.shuiyinyu.com
^https?:\/\/dashen.*\.shuiyinyu\.com\/.+\/user\/get_user_info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/dssy.js

#************************************#
# 电视家
# hostname = share.dianshihome.com, api.gaoqingdianshi.com, 123.56.125.184
^http[s]?:\/\/(share\.dianshihome\.com\/api\/user\/base\/info|123\.56\.125\.184\/api\/.+\/user\/info|api\.gaoqingdianshi\.com\/api\/ad\/mobile\/config) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/dsj.js

#************************************#
# 极简扫描
# hostname = cn.czur.cc
^https?:\/\/cn\.czur\.cc\/api\/.+\/User\/info?(.*?) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/jjsm.js
 
#************************************#
# PhotoSlip-照片清理大师
# hostname = www2.tigeroom.com
^https?:\/\/www2\.tigeroom\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/zpqlds.js

#************************************#
# 猫头鹰文件管理
# hostname = www.skyjos.cn
^https?:\/\/www\.skyjos\.cn url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mtywj.js

#************************************#
# 爱剪辑
# hostname = api.open.loveclip.site
^https?:\/\/api\.open\.loveclip\.site\/UserInfo\/(UserPersonalCoreAsync|GetUserDetail) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/ajj.js

#************************************#
# 六个解锁合集（Collart，拼图趣，睡前故事大全，网速测速大师，测速管家，Pixelance）
# hostname = iap.etm.tech
^https?:\/\/iap\.etm\.tech\/receipts url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Collart.js

#************************************#
# TopWidgets万能小组件
# hostname = top-widgets-api.xiaozujian.com
^https?:\/\/top-widgets-api\.xiaozujian\.com\/api\/app\/config\/userConfig url script-response-body https://raw.githubusercontent.com/89996462/Quantumult-X/main/ycdz/widgets.js

#************************************#
# 极简汇率
# hostname = xremit.xcurrency.com, explorer.tratao.com
^https?:\/\/(xremit\.xcurrency|explorer.tratao)\.com\/api\/client\/xtool\/vip url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/jijianhuilv.js

#************************************#
# AdGuard
# hostname = mobile-api.adguard.org
^https?:\/\/mobile-api\.adguard\.org\/api\/.+\/ios_validate_receipt\/(.*?) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/AdGuard.js

#************************************#
# 番薯小说
# hostname = ggs.manmeng168.com
^https?:\/\/ggs\.manmeng168\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/fanshuxiaoshuo.js

#************************************#
# 阅读记录
# hostname = app.yidiansz.com
^https?:\/\/app\.yidiansz\.com\/api\/.+\/app\/user\/info?(.*?)*$ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/ydjl.js

#************************************#
# Wink，蛋啵，潮自拍，海报工厂，Chic
# hostname = api-*.meitu.com
^https?:\/\/api-.*\.meitu\.com\/(.+\/user\/vip_info|user\/show) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mtxl.js

#************************************#
# 美颜相机
# hostname = *.meiyan.com
^https?:\/\/(api|community)\.meiyan\.com\/(vip|v\d)\/(user_center|user_info|user\/(.*?)) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/myxj.js

#************************************#
# 美图秀秀
# hostname = *.xiuxiu.meitu.com, api.posters.meitu.com, api-*.meitu.com
^https?:\/\/((h5|api)\.xiuxiu|api-sub|api\.posters)\.meitu\.com\/.+\/(vip|user|h\d|center|home) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mtxx.js

#************************************#
# Fimo_复古胶片相机
# hostname = server.*.com
^https?:\/\/server\.(yoyiapp|zbisq)\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/fimo.js

#************************************#
# 小习惯-打卡App
# hostname = xianbeikeji.com
^https?:\/\/xianbeikeji\.com\/daily\/app\/user\/query url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/xxg.js

#************************************#
# Mate-翻译神器
# hostname = asia.gikken.co
^https?:\/\/asia\.gikken\.co\/matesync\/(subscription|login|register_user|check_user) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mate.js

#************************************#
# 得间小说
# hostname = dj.palmestore.com
^https?:\/\/dj\.palmestore\.com\/zyuc\/api\/user\/accountInfo url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/dejianxiaoshuo.js

#************************************#
# Moji辞书-学习日语
# hostname = api.mojidict.com
^https?:\/\/api\.mojidict\.com\/parse\/functions\/getNPrivileges url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mojics.js

#************************************#
# Batched-多量图片编辑器
# hostname = api.adapty.io
^https:\/\/api\.adapty\.io\/api\/.+\/sdk\/(analytics\/profiles\/(.*?)\/|in-apps\/(apple\/receipt\/validate\/|purchase-containers\/.+)|events) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Batched.js

#************************************#
# 倒数纪念日
# hostname = day-api.xixitime.com
^https?:\/\/day-api\.xixitime\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/dsjnr.js

#************************************#
# 青柠设计-P图抠图海报
# hostname = *.qingning6.com
^https?:\/\/.*\.qingning6\.com\/api\/(user\/getUserInfo|team\/teamInfo) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/qnsj.js

#************************************#
# 配音秀
# hostname = iosapi.peiyinxiu.com
^https?:\/\/iosapi\.peiyinxiu\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/peiyinxiu.js

#************************************#
# 蓝基因
# hostname = *.lanjiyin.com.cn
^https?:\/\/tk\.lanjiyin\.com\.cn\/img url reject
^https?:\/\/(tk|course)\.lanjiyin\.com\.cn url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/lanjiyin.js

#************************************#
# 一天阅读(新版已失效)
# hostname = novel.test.onedayapp.cn
^https?:\/\/novel\.test\.onedayapp\.cn\/login\/sync.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yitianyuedu.js

#************************************#
# 小时尚
# hostname = kongque.twan.cn
^https?:\/\/kongque\.twan\.cn\/index.+\/admin\/appberrycustomer.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/xiaoshishang.js

#************************************#
# 计算器HD，万能播放器，万能变声器，塔罗牌，Art Widget(小组件)，memo(标签小组件)，NFC标签读写器工具，(一共解锁七个App)
# hostname = www.40sishi.com
^http[s]?:\/\/www\.40sishi\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/40sishi.js

#************************************#
# 薄荷健康
# hostname = api.boohee.com
^https?:\/\/api\.boohee\.com\/app-interface\/.+\/user\/user_info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/bohejiankang.js

#************************************#
# 菜谱大全，烘焙小屋，香哈菜谱
# hostname = *.xiangha.com
^https?:\/\/api.*\.xiangha\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/caipu.js

#************************************#
# 排班日历-倒班助手
# hostname = schedule-api.julanling.com
^https?:\/\/schedule-api\.julanling\.com\/api\/(get_member_info|vip_detail) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/paibanrili.js

#************************************#
# Xmind-思维导图
# hostname = *xmind.*
^https?:\/\/(?:www\.)?xmind\..*\/.+\/(devices|token\/.+) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Xmind.js

#************************************#
# 靓机汇
# hostname = guapi.liangjihui.com, ljh.dianxiaoman.com
^https?:\/\/guapi\.liangjihui\.com\/(front\/(quote\/look.+|user\/memberInfo)|api) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/liangjihui.js
^https?:\/\/ljh\.dianxiaoman\.com\/ljh\/api\/home\/getHomeList url reject

#************************************#
# 挖财记账
# hostname = jz.wacai.com
^https?:\/\/jz\.wacai\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/wacaijizhang.js

#************************************#
# 野果阅读
# hostname = yeguo.236api.com
^https?:\/\/yeguo\.236api\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yeguoyuedu.js

#************************************#
# 夸克
# hostname = drive*.quark.cn
^https?:\/\/drive.*\.quark\.cn\/.+\/clouddrive\/(member.+|distribute\/detail.+|capacity\/growth\/info) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/kuake.js

#************************************#
# 蜗牛睡眠
# hostname = snailsleep.net
^https?:\/\/snailsleep\.net\/snail\/v\d\/profile\/get.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/woniushuimian.js

#************************************#
# 网易蜗牛读书
# hostname = p.du.163.com
^https?:\/\/p\.du\.163\.com\/gain\/readtime\/info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/wywnds.js

#************************************#
# DailyArt(每日艺术)
# hostname = api.getdailyart.com
^https?:\/\/api\.getdailyart\.com\/api\/(subscription\/verified|auth\/login|check-logged) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/DailyArt.js

#************************************#
# 录屏，大神P图，乐秀，多功能视频剪辑
# hostname = *.videoshowiosglobalserver.com, *.enjoy-mobi.com
^https?:\/\/.*\.(videoshowiosglobalserver|enjoy-mobi)\.com\/zone\/.+\/(iosPayClient\/(payVerify|imeiVerify)|startPageAd\/getAds) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/VideoShow.js

#************************************#
# iTranslate 翻译
# hostname = ssl-api.itranslateapp.com
^https?:\/\/ssl-api\.itranslateapp\.com\/accounts\/.+\/(subscriptions\/verify|marketing\/consent\/status) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/itranslate.js

#************************************#
# Icon Killer，字体册，充电助手，声波助手
# hostname = api.yonekura.cn
^https?:\/\/api\.yonekura\.cn\/.+\/uicommon\/getuser url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yonekura.js

#************************************#
# 图纸通
# hostname = api.tuzhitong.com
^https?:\/\/api\.tuzhitong\.com\/api\/User\/GetUserVipInfo url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/tuzhitong.js

#************************************#
# Calendars 日历/计划
# hostname = license.pdfexpert.com
^https?:\/\/license\.pdfexpert\.com\/api\/.+\/calendarslite\/subscription\/refresh url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/calendars.js

#************************************#
# 微信听书
# hostname = i.at.qq.com
^https?:\/\/i\.at\.qq\.com\/pay\/memberinfo.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/wxts.js

#************************************#
# 冥想星球
# hostname = kc.xinli001.com
^https?:\/\/kc\.xinli001\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mingxiangxingqiu.js

#************************************#
# WPS Office
# hostname = *.wps.cn
^https?:\/\/(vas|account|drive)\.wps\.cn\/(query\/api\/.+\/list_purchase_info|api\/(v\d\/spaces|users\/.+\/overview)) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/WPS.js

#************************************#
# 墨迹天气
# hostname = *.api.moji.com
^http?:\/\/oss4bpc\.moji\.com\/.\d+\/.\d+\/.\d+\/.+\.jpg url reject
^https?:\/\/.*\.api\.moji\.com\/(sns\/json\/profile\/get_info_.+|json\/member_new\/homepage_info.+|user\/personal\/json\/profile_.+|flycard\/novice|shortvideo\/.+) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mojitianqi.js

#************************************#
# Pixelup AI照片增强器
# hostname = receipt-verifier.cdwapi.com
^https?:\/\/receipt-verifier\.cdwapi\.com\/receipt url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Pixelup.js

#************************************#
# iScreen小组件-辅助解锁
# hostname = *.kuso.xyz
^https?:\/\/pay\.kuso\.xyz\/pay\/pay-check url reject-200
# 备用方案，非一次性解锁
#^https?:\/\/cs\.kuso\.xyz\/configs.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/iscreenfz.js

#************************************#
# 旅途随身听
# hostname = www.1314zhilv.com
^https?:\/\/www\.1314zhilv\.com\/ltsstnew\/(user.*\/getInfo|guideScenic) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/ltsst.js

#************************************#
# 问真排盘
# hostname = bzpp2.iwzbz.com
^https?:\/\/bzpp2\.iwzbz\.com\/api\/.+\/(user\/getvipinfo|User\/getWXPW) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/wenzhenpaipan.js

#************************************#
# 经济学人·商论
# hostname = api.hummingbird.businessreview.global
^https:\/\/api\.hummingbird\.businessreview\.global\/api\/subscriptions\/get_active url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/jjxrsl.js

#************************************#
# 有谱么
# hostname = yopu.co
^https?:\/\/yopu\.co\/api\/user\/info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/youpume.js

#************************************#
# CAD快速看图
# hostname = cad.glodon.com
^https?:\/\/cad\.glodon\.com\/(account|authorize\/query|alipay\/auth) url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/cad.js

#************************************#
# 过期啦
# hostname = api.guoqi365.com
^https:\/\/api\.guoqi365\.com\/.+\/functions\/getUserInfo url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/guoqila.js

#************************************#
# flapp
# hostname = fl*app.com
^https:\/\/fl.*app\.com\/api\/v\d\/user\/me url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/lofo.js

#************************************#
# Hyperweb Safari浏览器扩展
# hostname = zy6kcqa01a.execute-api.us-east-2.amazonaws.com
^https?:\/\/zy6kcqa01a\.execute-api\.us-east-2\.amazonaws\.com\/prod\/verifyReceipt url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Hyperweb.js

#************************************#
# TimeTree日历
# hostname = api.timetreeapp.com
^https?:\/\/api\.timetreeapp\.com\/.+\/user\/.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/TimeTree.js

#************************************#
# 日历假期
# hostname = calendar.aiyohoo.com
^https?:\/\/calendar\.aiyohoo\.com\/api\/.+\/(user\/device|calendar\/dev_auth) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/rljq.js

#************************************#
# MorpholidTrace-CAD草图设计
# hostname = www.mymorpholio.com
^https:\/\/www\.mymorpholio\.com\/api\/index\.php\/rest_iap\/receipt url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/MorpholioTrace.js

#************************************#
# Notability
# hostname = notability.com
^https?:\/\/notability\.com\/(global|subscriptions) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/notability.js

#************************************#
# 解锁10个APP，包含APP：Filmicpro，Focos，Focos live，Splice，30 Day Fitness，Sleep，Remini，Yoga Wave，Firstlight，Doubletake
# hostname = *.oracle.bendingspoonsapps.com
^https?:\/\/.*\.oracle\.bendingspoonsapps\.com\/v\d\/(users\/.+|purchases\/verify) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/bending.js

#************************************#
# 考途大学搜题
# hostname = api-service.tutusouti.com 
^https:\/\/api-service\.tutusouti\.com\/appServiceApi\/(vip\/newUserPayVipData|video\/videoDetail) url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/kaotu.js

#************************************#
# Endel
# hostname = api-production.endel.io
^https?:\/\/api-production\.endel\.io\/v\d\/call url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Endel.js

#************************************#
# 格志日记
# hostname = diary-id.sumi.io
^https?:\/\/diary-id\.sumi\.io\/api\/profile url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/gezhi.js

#************************************#
# Tripsy-旅行规划者
# hostname = firstclass.tripsy.app
^https?:\/\/firstclass\.tripsy\.app\/api\/.+\/receipt\/update url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/tripsy.js

#************************************#
# 泼辣修图
# hostname = api.polaxiong.com
^https?:\/\/api\.polaxiong\.com\/.+\/payments\/(profiles\/.+\/subscription|appleiap\/receipts\/confirmation) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/pola.js

#************************************#
# gg
# hostname = isi.*.g*.com*
^https:\/\/isi\..*\.g.*\.(com\..*|com)\/.+\/(receipts$|subscribers\/?(.*?)*$) url script-response-body http://git.yycm.link/chxm1023/Rewrite/raw/main/gg.js
^https:\/\/isi\..*\.g.*\.(com\..*|com)\/.+\/(receipts$|subscribers\/?(.*?)*$) url script-request-header http://git.yycm.link/chxm1023/Rewrite/raw/main/gg.js

#************************************#
# 牛津高阶词典第十版
# hostname = oxfordx.cp.com.cn
^https:\/\/oxfordx\.cp\.com\.cn\/api\/pay\/apple_notify url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/niujin10.js
# 牛津高阶词典-去除首页下方广告
^https:\/\/oxadmin\.cp\.com\.cn\/api\/(hot\/index|advertise\/banner) url reject-dict

#************************************#
# Flightradar24
# hostname = mobile.flightradar24.com
^https:\/\/mobile\.flightradar24\.com\/mobile\/(user-session|subscribe) url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/Flightradar24.js

#************************************#
# 时光手帐
# hostname = api.shouzhang.com
^https:\/\/api\.shouzhang\.com\/memcenterlk\/member\/firstpage\.do url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/shiguangshouzhang.js

#************************************#
# 时光序
# hostname = api.weilaizhushou.com
^https:\/\/api\.weilaizhushou\.com\/base\/user\/vip\/getUserVip url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/shiguangxu.js

#************************************#
# 人人视频
# hostname = api.hujuvod.com, api.qwapp.top
^https?:\/\/api\.(hujuvod\.com|qwapp\.top)\/(user\/personal\/information|app\/drama\/page) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/renrenshipin.js

#************************************#
# Anki记忆卡
# hostname = api.ankichinas.com
^https:\/\/api\.ankichinas\.com\/api\/.+\/users\/vipInfo url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/Anki.js

#************************************#
# 心脏+
# hostname = api.995120.cn
^https:\/\/api\.995120\.cn\/mini\/api\/appleplus url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/xinzang.js

#************************************#
# 记乎
# hostname = api.geefoo.cn
^https:\/\/api\.geefoo\.cn\/.+\/account\/userinfo url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/jihu.js

#************************************#
# Promova
# hostname = api.panda.boosters.company
^https:\/\/api\.panda\.boosters\.company\/.+\/subscription-status url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/Promova.js

#************************************#
# 音频剪辑大师
# hostname = www.tingniukeji.com
^http:\/\/www\.tingniukeji\.com\/audioclip\/queryIosVip url script-echo-response https://raw.githubusercontent.com/Yu9191/Rewrite/main/ypjjds.js

#************************************#
# 刷刷题
# hostname = api.shuashuati.com
^https?:\/\/api\.shuashuati\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/shuashuati.js

#************************************#
# 驾考宝典
# hostname = *.kakamobi.cn
^https?:\/\/.*\.kakamobi\.cn\/api\/open url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/jiakaobaodian.js

#************************************#
# 指尖时光
# hostname = integral2.dasyibalang.com
^https?:\/\/integral2\.dasyibalang\.com\/.+\/User url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/zjsg.js

#************************************#
# exping地图标记
# hostname = api.expingworld.com
^https?:\/\/api\.expingworld\.com\/users url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/exping.js

#************************************#
# 360相机
# hostname = *.camera360.com
^https?:\/\/.*\.camera360\.com\/(api\/(order\/purchase|iap\/check-receipt)|v\d\/operational-positions) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/360xj.js

#************************************#
# 一键抠图
# hostname = api.mattingm.com
^https?:\/\/api\.mattingm\.com\/receipt_api\/user\/info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yijiankoutu.js

#************************************#
# 畅玩空间
# hostname = play.wo1wan.com
^https?:\/\/play\.wo1wan\.com\/nextgame\/igwuser\/userinfo url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/changwan.js

#************************************#
# 随手写
# hostname = www.kkmop.com
http:\/\/www\.kkmop\.com\/vipMsg1 url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/suishouxie.js

#************************************#
# 悄悄朋友圈
# hostname = qqpyqapi.app.xinmaicard.com
^http?:\/\/qqpyqapi\.app\.xinmaicard\.com\/user\/auth_userinfo.*? url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/pyq.js

#************************************#
# 杂志天下
# hostname = www.fuyoutech.club
^https?:\/\/www\.fuyoutech\.club\/magworld\/member\/status url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/zztx.js

#************************************#
# 建工计算器
# hostname = calc.kuaicad.com
^https:\/\/calc\.kuaicad\.com\/authority\/verify_vip url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/jiangongjsq.js

#************************************#
# Koan-提问日记
# hostname = koan.bopulab.cn
^https?:\/\/koan\.bopulab\.cn\/(user\/getBriefByUserIdV3|payment\/iosIap\/receipt) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/koan.js

#************************************#
# 一飞记账
# hostname = jz.jarstones.com
^https?:\/\/jz\.jarstones\.com\/api url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yifeijizhang.js

#************************************#
# Lambus-(美区下载)
# hostname = prod.api.lambus.io
^https:\/\/prod\.api\.lambus\.io\/v\d\.+\/subscriptions url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/Lambus.js

#************************************#
# 恋小语
# hostname = api.love.823123.com
# 去广告
^http:\/\api\.love\.823123\.com\/facades\/ad_space\.index url reject-200
# VIP显示
^http:\/\/api\.love\.823123\.com\/facades\/account\.show$ url script-response-body https://raw.githubusercontent.com/wf021325/qx/master/js/lxy.js
# 小恋老师，键盘-回复它-开场白
^http:\/\/api\.love\.823123\.com\/(facades\/open\.chat_stream|v1\/discovery\/query) url script-request-header  https://raw.githubusercontent.com/wf021325/qx/master/js/lxy.js

#************************************#
# 养基宝
# hostname = *.yangjibao.com
^https?:\/\/.*\.yangjibao\.com url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yjb.js

#************************************#
# 恋知道
# hostname = api.lianzhidao123.com
^http?:\/\/api\.lianzhidao123\.com\/v2\/account.*? url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/lianzhidao.js

#************************************#
# GUGA白板
# hostname = www.guga.co
^https?:\/\/www\.guga\.co\/api-base\/v2\/(state|preferential-product) url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/GUGA.js

#************************************#
# Drafts
# hostname = backend.getdrafts.com
^https?:\/\/backend\.getdrafts\.com\/api\/v\d\/verification\/(account_status|verify_receipt) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Drafts.js

#************************************#
# 17个APP合集，
# hostname = *api.quthing.com
^https:\/\/.*api\.quthing\.com\/(.+\/vip|vip|student|user|appearance|background|rest) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yueqi.js

#************************************#
# Hydra相机
# hostname = creaceed.com
^https?:\/\/creaceed\.com\/apis\/appstore\/verifyreceipt url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Hydra.js

#************************************#
# Scientific_American杂志
# hostname = main-sciam-nature.content.pugpig.com
^https:\/\/main-sciam-nature\.content\.pugpig\.com\/subs\/(itunes_store|pianomediaoauth_subs)\/verify_subscription url script-response-body https://raw.githubusercontent.com/leey668/pyer/main/sa.js

#************************************#
# DayMore-时尚日记本
# hostname = *.execute-api.ap-northeast-2.amazonaws.com
^https?:\/\/.*\.execute-api\.ap-northeast-2\.amazonaws\.com\/product\/apple\/receipt url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/daymore.js

#************************************#
# Noted录音笔记软件
# hostname = subscription-api.notedapp.io
^https:\/\/subscription-api\.notedapp\.io\/api\/verifyReceipt url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Noted.js

#************************************#
# 爱涂绘画
# hostname = kkr-user.tapque.com
^https?:\/\/kkr-user\.tapque\.com\/kkruserapi\/userOrderInfo\/isVip url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/aituhuihua.js

#************************************#
# 一起练琴
# hostname = api.*lianqin*.*, api.mangofuture.cn
^https?:\/\/api\.(.*lianqin.*|mangofuture)\.(com|cn)\/client\/v\d\/(user_vip|my_info) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/yiqilianqin.js

#************************************#
# Foodie/轻图/B612相机/甜盐相机
# hostname = purchase-*-api.*.com, user-kaji-api.b612kaji.com
^https?:\/\/(purchase-.*-api|user-kaji-api)\.(yiruikecorp|b612kaji|tianyancam)\.com\/v\d\/purchase\/subscription\/subscriber\/status url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/4gexj.js

#************************************#
# 13个APP解锁全家桶
# hostname = standard.rhinox*.com, appss.rhinox*.com, appss.linhongshi.com
^https?:\/\/(appss|standard)\.(rhinox.*|linhongshi)\.com\/.+\/account\/getAccountInfo url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/13geapp.js

#************************************#
# FT中文网/RainViewer天气预报
# hostname = *.cloudfront.net, ftmailbox.cn
^https?:\/\/.*\.cloudfront\.net\/(index\.php\/jsapi\/(paywall|get_story_more_info)|mobile\/verify) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/cloudfront.js
^https?:\/\/ftmailbox\.cn\/ad_impression url reject-200

#************************************#
# 水印宝/闪电水印/熊猫水印/水印全能王
# hostname = water*.yunxiaoguo.cn
^https?:\/\/water.*\.yunxiaoguo\.cn\/user\/info url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/shuiyin.js

#************************************#
# 消防行
# hostname = www.xfx119.com
^https?:\/\/www\.xfx119\.com\/ksVRExamSystem\/validityTerm url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/xiaofangxing.js

#************************************#
# Vista看天下
# hostname = open3.vistastory.com
^https?:\/\/open3\.vistastory\.com\/v\d\/api\/(vip|my\/home\/get_home_center|user/pendant|poster\/share_poster|adm\/get_popup_ad|index\/loading_ad) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/Vista.js

#************************************#
# 暴走P图
# hostname = api.intelimeditor.com
^https?:\/\/api\.intelimeditor\.com\/user\/loginByThirdPlatformApp url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/baozouptu.js

#************************************#
# Glass:摄影社区
# hostname = glass.photo
^https:\/\/glass\.photo\/api\/(v2\/users\/[0-9a-zA-Z-]+$|v1\/account$|v3\/token$) url script-response-body https://raw.githubusercontent.com/leey668/pyer/main/glass.js

#************************************#
# 星题库
# hostname = cm15-c110-3.play.bokecc.com,  mb.xinghengedu.com
# 会员
^https?:\/\/mb\.xinghengedu\.com\/api\/.+\/getUserByToken\.do url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/Xingtiku.js
# 题库
^https?:\/\/cm15-c110-3\.play\.bokecc\.com\/flvs url script-request-header https://raw.githubusercontent.com/Yu9191/Rewrite/main/Xingtikukecheng.js

#************************************#
# 七天学堂
# hostname = szone-my.7net.cc
^https?:\/\/szone-my\.7net\.cc\/userInfo\/GetUserInfo url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/Qitianxuetang.js

#************************************#
# MIX-滤镜大师
# hostname = cdn-bm.camera360.com
^https?:\/\/cdn-bm\.camera360\.com\/api\/(mix\/(getinfo|purchase|recovery)|iap\/check-receipt) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/mix.js

#************************************#
# 扫描宝
# hostname = app.yinxiang.com
# 资料
^https?:\/\/app\.yinxiang\.com\/third\/profile\/public\/restful\/public-user-profile url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/saomiaobao.js
# 会员
^https?:\/\/app\.yinxiang\.com\/third\/scanner\/scanner\/app\/userInfo\/get url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/saomiaobao2.js

#************************************#
# 陆琪讲故事
# hostname = www.luqijianggushi.com
^https?:\/\/www\.luqijianggushi\.com\/api url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/luqijianggushi.js

#************************************#
# Tidal音乐
# hostname = api.tidal.com
^https?:\/\/api\.tidal\.com\/v1\/users\/\d+\/subscription.+ url script-response-body https://raw.githubusercontent.com/yqc007/QuantumultX/master/TIDALHiFiPlusCrack.js
^https?:\/\/api\.tidal\.com\/v1\/tracks/\d+\/playbackinfopostpaywall.+ url script-analyze-echo-response https://raw.githubusercontent.com/Yuheng0101/X/main/Scripts/TIDAL/tidal.js

#************************************#
# codesnackide 软件开发工具
# hostname = api.cs-ide.io
^https?:\/\/api\.cs-ide\.io\/purchases\/active url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/codesnackide.js

#************************************#
# 小熊油耗
# hostname = www.xiaoxiongyouhao.com
^https?:\/\/www\.xiaoxiongyouhao\.com\/api\/vip\/index.+ url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/xiaoxiongyouhao.js

#************************************#
# Slidebox相册清理
# hostname = *-slidebox-ios-prod.cloudfunctions.net
^https?:\/\/.*-slidebox-ios-prod\.cloudfunctions\.net\/api.+ url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/slidebox.js

#************************************#
# 板凳音乐
# hostname = mobileapp.wuyamusic.com
^https?:\/\/mobileapp\.wuyamusic\.com\/playmusic-app-server-400\/(vip\/user\/list.+|music\/score\/get2.+|choose\/getmusic|api|app\/swiper) url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/bandeng.js

#************************************#
# 灵兰中医
# hostname = user.linglan.com
^https?:\/\/user\.linglan\.com\/api\/personCenter\/getMyUser url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/linglanzhongyi.js

#************************************#
# 小歪微商
# hostname = xw.jietuguanjia.com
http:\/\/xw\.jietuguanjia\.com\/api\/app\/userInfo url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/xiaowaiweishang.js

#************************************#
# Replica-屏幕镜像
# hostname = api.apphud.com
^https?:\/\/api\.apphud\.com\/v1\/subscriptions url script-response-body https://raw.githubusercontent.com/chxm1023/Rewrite/main/replica.js

#************************************#
# 闪萌表情
# hostname = hi-api.weshineapp.com
^https?:\/\/hi-api\.weshineapp\.com\/.+\/account\/profile url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/shanmengbiaoqing.js

#************************************#
# 万兴喵影
# hostname = api.300624.com
^https?:\/\/api\.300624\.com\/v3\/plan\/feature-code\/auth url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/wanxingmiaoying.js

#************************************#
# 糖豆-广场舞教学视频
# hostname = *.tangdou.com
^https:\/\/.*\.tangdou\.com\/(?:\w*\/)?\d+\/\d+_\w+\.mp4\?sign=[\w-]+&t=\w+$ url script-request-header https://raw.githubusercontent.com/Yu9191/Rewrite/main/Tangdou.js



#************************************#
hostname = *.tangdou.com, api.300624.com, hi-api.weshineapp.com, api.apphud.com, xw.jietuguanjia.com, user.linglan.com, mobileapp.wuyamusic.com, *-slidebox-ios-prod.cloudfunctions.net, www.xiaoxiongyouhao.com, api.cs-ide.io, api.tidal.com, www.luqijianggushi.com, app.yinxiang.com, cdn-bm.camera360.com, szone-my.7net.cc, cm15-c110-3.play.bokecc.com, mb.xinghengedu.com, glass.photo, api.intelimeditor.com, open3.vistastory.com, www.xfx119.com, water*.yunxiaoguo.cn, *.cloudfront.net, ftmailbox.cn, standard.rhinox*.com, appss.rhinox*.com, appss.linhongshi.com, purchase-*-api.*.com, user-kaji-api.b612kaji.com, api.*lianqin*.*, api.mangofuture.cn, kkr-user.tapque.com, subscription-api.notedapp.io, *.execute-api.ap-northeast-2.amazonaws.com, main-sciam-nature.content.pugpig.com, creaceed.com, *api.quthing.com, backend.getdrafts.com, www.guga.co, api.lianzhidao123.com, *.yangjibao.com, api.love.823123.com, prod.api.lambus.io, jz.jarstones.com, koan.bopulab.cn, calc.kuaicad.com, www.fuyoutech.club, qqpyqapi.app.xinmaicard.com, www.kkmop.com, play.wo1wan.com, api.mattingm.com, *.camera360.com, api.expingworld.com, integral2.dasyibalang.com, *.kakamobi.cn, api.shuashuati.com, www.tingniukeji.com, api.panda.boosters.company, api.geefoo.cn, api.995120.cn, api.ankichinas.com, api.hujuvod.com, api.qwapp.top, api.weilaizhushou.com, api.shouzhang.com, mobile.flightradar24.com, oxfordx.cp.com.cn, isi.*.g*.com*, api.polaxiong.com, firstclass.tripsy.app, diary-id.sumi.io, api-production.endel.io, api-service.tutusouti.com, *.oracle.bendingspoonsapps.com, notability.com, www.mymorpholio.com, calendar.aiyohoo.com, api.timetreeapp.com, zy6kcqa01a.execute-api.us-east-2.amazonaws.com, fl*app.com, api.guoqi365.com, cad.glodon.com, yopu.co, api.hummingbird.businessreview.global, bzpp2.iwzbz.com, www.1314zhilv.com, *.kuso.xyz, receipt-verifier.cdwapi.com, *.api.moji.com, *.wps.cn, kc.xinli001.com, i.at.qq.com, license.pdfexpert.com, api.tuzhitong.com, api.yonekura.cn, ssl-api.itranslateapp.com, *.videoshowiosglobalserver.com, *.enjoy-mobi.com, api.getdailyart.com, p.du.163.com, snailsleep.net, drive*.quark.cn, yeguo.236api.com, jz.wacai.com, ljh.dianxiaoman.com, guapi.liangjihui.com, *xmind.*, schedule-api.julanling.com, *.xiangha.com, api.boohee.com, www.40sishi.com, kongque.twan.cn, ggs.manmeng168.com, novel.test.onedayapp.cn, *.lanjiyin.com.cn, iosapi.peiyinxiu.com, *.qingning6.com, day-api.xixitime.com, api.adapty.io, api.mojidict.com, dj.palmestore.com, asia.gikken.co, xianbeikeji.com, server.*.com, *.xiuxiu.meitu.com, api.posters.meitu.com,api-*.meitu.com,  *.meiyan.com, app.yidiansz.com, mobile-api.adguard.org, xremit.xcurrency.com, explorer.tratao.com, top-widgets-api.xiaozujian.com, iap.etm.tech, api.open.loveclip.site, www.skyjos.cn, www2.tigeroom.com, cn.czur.cc, share.dianshihome.com, api.gaoqingdianshi.com, 123.56.125.184, dashen*.shuiyinyu.com, *.imendon.com, api2.vlognow.me, service.ilovepdf.com, www.freshhome.top, *.dicallapp.com, format-api.netpock.com, widget-box-api.codefuture.top, cubox.*, *.radio.cn, 60.205.171.165, accounts.agenda.com, *.aoscdn.com, *.apsapp.cn, apimboom2.globaldelight.net, *.duitang.com, spclient.wg.spotify.com, scibug.com, *.wallpaperscraft.com, screen-lock.*.com, api.risingfalling.com, api.meiease.cn, *.aliyundrive.com, *.alipan.com, pan.baidu.com, *.camscanner.com, *.intsig.net, mb3admin.com, *.kuwo.cn, *.kwcdn.kuwo.cn, *.lrts.me, iosv2.cjapi.5fun.com, api*.speedtest.cn, app.yiyan.art, *.cyapi.cn, *.caiyunapp.com, adx.sogaha.cn, lcs-mobile-cops.adobe.io, wallpaper.soutushenqi.com, api.bluepulse.cn, restore-access.indream.app, buy.itunes.apple.com, api.revenuecat.com