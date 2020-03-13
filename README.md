解决梯子在GFWList模式下不能正常看流媒体的问题
 2019-10-15   |    0 评论   |    7390 浏览
问题场景：
客户端使用GFWList模式时观看流媒体。

问题描述：
当使用全局模式或大陆白名单模式时，可以观看流媒体
当使用GFWList模式时，无法观看（例如HBO NOW）
当使用GFWList模式时，可以观看，但有卡顿（例如YouTube）

HBO NOW在GFWList下的报错 Not in Service Area
问题分析：
流媒体CDN服务器的域名被GFWList识别为大陆网站。

若CDN服务区的域名不通过proxy访问，而是直达，流媒体网站可能会判定此连接非法。

解决方案：
添加相关域名至GFW列表（不同平台客户端的称谓不同）

Windows客户端配置：
编辑Windows客户端文件夹中的user-rules.txt


输入相应域名（格式为||域名），保存文件


选择PAC – 更新PAC为GFWList


重新连接，即可正常观看HBO NOW


结语：
GFW列表并不完整，遇到类似问题，可能需要通过抓包来找出其中缺失的域名。

附：流媒体必须经过代理的域名
Netflix
fast.com
netflix.com
netflix.net
nflxext.com
nflximg.net
nflxso.net
nflxvideo.net
Amazon Prime
amazon.com
amazon.co.jp
amazon.co.uk
amazon.de
amazonvideo.com
primevideo.com
Twitch
twitch.tv

ttvnw.net

Turnin
turnin.com
amazon-adsystem.com
pubmatic.com
acast.com
adswizz.com
openx.net
crwdcntrl.net
agkn.com
radiotime.com
Line
line.me
naver.jp
主机游戏网络
playstation.net
xboxlive.com
部分第三方地址检测及防地址欺诈服务
maxmind.com
ifconfig.co
ip2location.com
uplynk.com
HBO NOW
conviva.com
go.com
hbo.com
hbogo.com
hbonow.com
Hulu
hulu.com
huluad.com
huluim.com
hulustream.com
Showtime
sho.com
showtime.com
DirecTV NOW
att.com
codec-cluster.org
conviva.com
directv.com
directvnow.com
dtvce.com
footprint.net
imrworldwide.com
inq.com
omtrdc.net
Sling TV
adrta.com
adsrvr.org
cloudfront.net
crashlytics.com
doubleverify.com
fwmrm.net
innovid.com
movetv.com
omtrdc.net
scorecardresearch.com
serving-sys.com
sling.com
spotxchange.com
tremorhub.com
videoamp.com
YouTube及YouTube TV
ggpht.com
googleapis.com
googletagmanager.com
googleusercontent.com
googlevideo.com
gstatic.com
imrworldwide.com
ytimg.com
youtube.com
部分美国电视台
abc.com
amctv.com
beinsportsconnect.net
beinsportsconnect.tv
cbs.com
cwtv.com
fox.com
mtv.com
mtvnservices.com
nbc.com
nbcuni.com
pbs.org
BBC iPlayer
bbc.co.uk
linwd.net
爱奇艺（配置后会影响观看内容）
iqiyi.com
巴哈姆特動畫瘋
gamer.com.tw
bahamut.com.tw
hinet.net
fbcdn.net
gvt1.com
digicert.com
viblast.com
Line TV
line.me
line-apps.com
GYAO!
yahoo.co.jp
yimg.jp
brightcove.com
TVer
tver.jp
amazonaws.com
yahoo.co.jp
brightcove.com
AbemaTV(アベマTV)
abema.tv
ameblo.jp
akamaized.net
