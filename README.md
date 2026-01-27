#!name=掌上英雄联盟 去开屏广告
#!desc=拦截掌上英雄联盟开屏与推荐广告
#!author=你自己
#!homepage=https://github.com/yourname
#!icon=https://raw.githubusercontent.com/Orz-3/mini/master/Color/LOL.png

[Rule]
DOMAIN,us.l.qq.com,REJECT
DOMAIN,ossweb-img.qq.com,REJECT
DOMAIN,mlol.qt.qq.com,REJECT

[Rewrite]
# 开屏广告
^https?:\/\/us\.l\.qq\.com\/exapp reject

# 图片广告
^https?:\/\/ossweb-img\.qq\.com\/upload\/adw\/image\/[0-9]{3}\/202[0-9]{5}\/[a-z0-9]{32}\.(jpg|jpeg) reject

# 推荐广告（排除 v2/platactivity）
^https?:\/\/mlol\.qt\.qq\.com\/go\/recommend\/(?!v2\/platactivity.*) reject