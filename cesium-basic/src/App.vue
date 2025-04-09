<script setup>
import * as Cesium from 'cesium';
import "./Widgets/widgets.css";
import {onMounted} from "vue";

//设置cesium静态资源路径
window.CESIUM_BASE_URL = "/";

onMounted(()=>{
  var viewer=new Cesium.Viewer("cesiumContainer");
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
