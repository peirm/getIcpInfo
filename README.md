# 备案信息展示插件
# 备案信息展示插件 示例页面


# 示例代码
<div>
    <div><br></div><div>将以下代码放到需要显示的地方即可</div><div><br></div><div>&lt;script&gt;</div><div>!function(window) {</div><div>&nbsp; &nbsp; window.__GETICPINFO__ = {</div><div>&nbsp; &nbsp; &nbsp; &nbsp; websiteHost: '', // 不填将获取当前域名备案信息 这里可以填指定域名</div><div>&nbsp; &nbsp; &nbsp; &nbsp; jqueryPath: '', // 自定义jquery路径 之前有引入则不再引入 默认是bootcdn 可不用改</div><div>&nbsp; &nbsp; &nbsp; &nbsp; layerHeight: 'auto', // layer弹出层长度 默认自适应 可不用改</div><div>&nbsp; &nbsp; &nbsp; &nbsp; isCenter: false, // 是否居中 默认不居中 选择居中将单独占用一行</div><div>&nbsp; &nbsp; &nbsp; &nbsp; isShowInfo: true, // 是否点击备案号显示详细信息 false则不引入jquery和layer</div><div>&nbsp; &nbsp; &nbsp; &nbsp; showIcon: true, // 是否显示图标</div><div>&nbsp; &nbsp; &nbsp; &nbsp; icpIcon:"", // 自定义图标地址</div><div>&nbsp; &nbsp; &nbsp; &nbsp; removeDecoration: true, // 是否去掉a标签下划线 建议去掉比较美观</div><div>&nbsp; &nbsp; &nbsp; &nbsp; aColor: "", // 字体颜色</div><div>&nbsp; &nbsp; &nbsp; &nbsp; cacheTime: 1 // 缓存本地时间(防止重复获取拉低速度) 单位：天 默认1天</div><div>&nbsp; &nbsp; };</div><div>&nbsp; &nbsp; document.write('&lt;span id="icpInfoSpan"&gt;&lt;/span&gt;');</div><div>&nbsp; &nbsp; getIcpInfo_tag = document.createElement("script"),&nbsp;</div><div>&nbsp; &nbsp; getIcpInfo_tag.type = "text/javascript",&nbsp;</div><div>&nbsp; &nbsp; getIcpInfo_tag.async = true,&nbsp;</div><div>&nbsp; &nbsp; getIcpInfo_tag.src = "//api.yya.gs/Api/getIcpInfo"; // 代码频繁更新，建议不要弄到本地</div><div>&nbsp; &nbsp; var b = document.getElementsByTagName("script")[0];</div><div>&nbsp; &nbsp; b.parentNode.insertBefore(getIcpInfo_tag, b);</div><div>}(window);</div><div>&lt;/script&gt;</div><div>精简版，只显示备案号</div><div>&lt;script&gt;document.write(unescape("%3Cscript%20charset%3D%27utf-8%27%20src%3D%27https%3A//api.yya.gs/Api/getIcpInfoSimple%27%3E%3C/script%3E"));&lt;/script&gt;</div><div><br></div>
</div>
