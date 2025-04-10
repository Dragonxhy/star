<script setup>
import * as Cesium from 'cesium';
import "./Widgets/widgets.css";
import {onMounted} from "vue";

//设置cesium静态资源路径
window.CESIUM_BASE_URL = "/";

onMounted(()=>{
  var viewer=new Cesium.Viewer("cesiumContainer",{
    homeButton : false,//地图导航
    infoBox: false,//信息框
    sceneModePicker: false,//场景切换
    baseLayerPicker:false,//底图切换
    navigationHelpButton:false,//帮助
    geocoder:false,//地理搜索
    animation:false,//动画
    timeline:false,//时间线
    fullscreenButton:false//全屏
  });
  //隐藏logo
  viewer.cesiumWidget.creditContainer.style.display="none";
});
</script>

<template>
<div id="cesiumContainer" ref="cesiumContainer"></div>
</template>

<style scoped>
* {
margin: 0;
padding: 0;
}
#cesiumContainer {
width: 100vw;
height: 100vh;
}
</style>
