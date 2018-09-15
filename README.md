# 备案信息展示插件

## 示例代码
<pre>
<script>
!function(window) {
    window.__GETICPINFO__ = {
        websiteHost: '', // 不填将获取当前域名备案信息 这里可以填指定域名
        jqueryPath: '', // 自定义jquery路径 之前有引入则不再引入 默认是bootcdn 可不用改
        layerHeight: 'auto', // layer弹出层长度 默认自适应 可不用改
        isCenter: false, // 是否居中 默认不居中 选择居中将单独占用一行
        isShowInfo: true, // 是否点击备案号显示详细信息 false则不引入jquery和layer
        showIcon: true, // 是否显示图标
        icpIcon:"", // 自定义图标地址
        removeDecoration: true, // 是否去掉a标签下划线 建议去掉比较美观
        aColor: "", // 字体颜色
        cacheTime: 1 // 缓存本地时间(防止重复获取拉低速度) 单位：天 默认1天
    };
    document.write('<span id="icpInfoSpan"></span>');
    getIcpInfo_tag = document.createElement("script"), 
    getIcpInfo_tag.type = "text/javascript", 
    getIcpInfo_tag.async = true, 
    getIcpInfo_tag.src = "https://api.yya.gs/Api/getIcpInfo"; // 代码频繁更新，建议不要弄到本地
    var b = document.getElementsByTagName("script")[0];
    b.parentNode.insertBefore(getIcpInfo_tag, b);
}(window);
</script>
</pre>

## 精简版，只显示备案号

<pre>
<script>document.write(unescape("%3Cscript%20charset%3D%27utf-8%27%20src%3D%27https%3A//api.yya.gs/Api/getIcpInfoSimple%27%3E%3C/script%3E"));</script>
</pre>
