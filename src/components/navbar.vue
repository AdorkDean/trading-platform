<template>
    <div id="navBar">
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
              <el-menu-item index="1"><router-link :to="{path:'/home', query: {}}"><img src="../assets/img/logo_bcex.jpg"></router-link></el-menu-item>
              <el-menu-item index="2"><router-link :to="{path:'/home', query: {}}">交易中心</router-link></el-menu-item>
              <el-menu-item index="3"><router-link :to="{path:'/help-center', query: {}}">帮助中心</router-link></el-menu-item>
              <el-menu-item index="4"><router-link :to="{path:'/news', query: {}}">公告中心</router-link></el-menu-item>
              <el-submenu index="5" show-timeout="0" hide-timeout="0">
                <template slot="title">最新活动</template>
                <el-menu-item index="5-1"><a href="#" target="_blank">矿机售卖</a></el-menu-item>
                <el-menu-item index="5-2"><a href="#" target="_blank">HOTC排名赛</a></el-menu-item>
                <el-menu-item index="5-3"><a href="#" target="_blank">DCON排名赛</a></el-menu-item>
                <el-menu-item index="5-4"><a href="#" target="_blank">SDD排名赛</a></el-menu-item>
                <el-menu-item index="5-5"><a href="#" target="_blank">SHE排名赛</a></el-menu-item>
                <el-menu-item index="5-6"><a href="#" target="_blank">AIT排名赛</a></el-menu-item>
              </el-submenu>
              <el-submenu index="6">
                <template slot="title" show-timeout="0" hide-timeout="0">法币交易</template>
                <el-menu-item index="6-1"><a href="#" target="_blank">CK.USD & ETH & BTC</a></el-menu-item>
                <el-menu-item index="6-2"><a href="#" target="_blank">代理充值</a></el-menu-item>
              </el-submenu>
              <el-submenu style="float:right;" show-timeout="0" hide-timeout="0" index="9">
                <template slot="title"><img style="width: 20px; height: 20px" src="../assets/img/icon-hk.png"></template>
                <el-menu-item style="text-align: center" index="8-1"><img style="width: 20px; height: 20px; margin-right:9px" src="../assets/img/icon-hk.png">香港</el-menu-item>
                <el-menu-item style="text-align: center" index="8-2"><img style="width: 20px; height: 20px; margin-right:9px" src="../assets/img/icon-en.png">英国</el-menu-item>
              </el-submenu>
              <el-menu-item style="float:right; padding-right: 5px;padding-left: 5px;" index="8"><a href="#" target="_blank">注册</a></el-menu-item>
              <el-menu-item style="float:right; padding-right: 5px;padding-left: 5px;" index="7"><a href="#" target="_blank">登陆</a></el-menu-item>
        </el-menu>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'navbar',
    mounted () {
    },
    computed: {
    },
    watch: {
    },
    data () {
        return {
            activeIndex: '1'
        }
    },
    components: {
    },
    methods: {
        handleSelect(key, keyPath) {
            console.log(key,keyPath);
        }
    }
}
</script>

<style lang="scss" scoped>
#navBar {
  z-index: 9999;
  position: relative;
}
</style>
