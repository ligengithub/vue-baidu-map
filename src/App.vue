<template>
    <div id="app">
        <!--    <img alt="Vue logo" src="./assets/logo.png">-->
        <!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->

        <!-- 注意 百度地图的应用类型分为  服务端，小程序端，androidSdk,IosSdk,浏览器端-->
        <!-- 在早些年，服务端的应用的key 同样也是支持浏览器端调用的，现在是不支持的，浏览器端使用的key需要在百度地图上创建浏览器端的应用，使用对应生成的key-->
        <!--如果地图不能加载出来， 1 请先上百度地图后台，检查应用类型，2 检查后天设备的ip白名单，服务端应用设置0.0.0./0 ，浏览器端的应用设置 * 来允许任何地址的请求。线上环境请设置服务器对应的地址 -->
        <baidu-map ak="yourkey" style="width: 100%; height: 800px; margin: auto" :center="{lng: 116.404, lat: 39.915}"
                   :zoom="15"></baidu-map>
    </div>
</template>

<script>
    // import HelloWorld from './components/HelloWorld.vue'
    import BaiduMap from 'vue-baidu-map/components/map/Map.vue'

    export default {
        name: 'App',
        components: {
            // HelloWorld,
            BaiduMap
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
