# 更新日志
2026-06-11：\
1.修复加载源后，首页左上角TVBox仍在闪烁的bug，并删除此按钮的红色包裹\
2.优化TVBox闪烁逻辑，加载源时开始闪烁，加载成功或失败、取消加载，停止闪烁\
3.隐藏顶部WiFi或有线网络图标，隐藏九宫格APP入口\
4.修改包名，避免与源APP无法同时安装\
5.使用临时签名，暂不适合分发，无法升级、覆盖安装


---------------------------------------------------------------------------------------------
# Box

=== Source Code - Editing the app default settings ===
/src/main/java/com/github/tvbox/osc/base/App.java

    private void initParams() { 

        putDefault(HawkConfig.HOME_REC, 2);       // Home Rec 0=豆瓣, 1=推荐, 2=历史
        putDefault(HawkConfig.PLAY_TYPE, 1);      // Player   0=系统, 1=IJK, 2=Exo
        putDefault(HawkConfig.IJK_CODEC, "硬解码");// IJK Render 软解码, 硬解码
        putDefault(HawkConfig.HOME_SHOW_SOURCE, true);  // true=Show, false=Not show
        putDefault(HawkConfig.HOME_NUM, 2);       // History Number
        putDefault(HawkConfig.DOH_URL, 2);        // DNS
        putDefault(HawkConfig.SEARCH_VIEW, 2);    // Text or Picture

    }
