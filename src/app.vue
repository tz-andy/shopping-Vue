<template>
    <div class="mainContainer">
        <mt-header fixed title="购物网-Vue项目"></mt-header>
        <transition>
            <router-view></router-view>
        </transition>
        <nav class="mui-bar mui-bar-tab">
            <router-link class="mui-tab-item" to="/home">
                <span class="mui-icon mui-icon-home"></span>
                <span class="mui-tab-label">首页</span>
            </router-link>
            <router-link class="mui-tab-item" to="/member">
                <span class="mui-icon mui-icon-contact"></span>
                <span class="mui-tab-label">会员</span>
            </router-link>
            <router-link class="mui-tab-item" to="/shopping">
                <span class="mui-icon mui-icon-extra mui-icon-extra-cart"><span class="mui-badge">0</span></span>
                <span class="mui-tab-label">购物车</span>
            </router-link>
            <router-link class="mui-tab-item" to="/search">
                <span class="mui-icon mui-icon-search"></span>
                <span class="mui-tab-label">搜索</span>
            </router-link>
        </nav>
    </div>
</template>

<script>
    export default {};
</script>

<style scoped lang="less">
    .mainContainer{
        padding-top: 40px;
        padding-bottom: 50px;
        overflow-x: hidden;
    }
    .v-enter{
        transform: translateX(100%);
        opacity: 0;
    }
    .v-leave-to{
        transform: translateX(-100%);
        opacity: 0;
        position: absolute;
    }
    .v-enter-active,
    .v-leave-active{
        transition: all 1s ease;
    }
</style>