<template>
    <div>
        <HeaderSearch ref="headerSearchrl"></HeaderSearch>
        <section class="m-content">
            <!-- <iframe src="http://www.baidu.com" frameborder="0" scrolling="no" ref="iframe"></iframe> -->
        </section>
    </div>
</template>

<script setup lang="ts">
import HeaderSearch from './components/HeaderSearch.vue';
import { ref } from 'vue';
</script>

<style scoped>
.m-content {
    width: 100vw;
    height: 90vh;
}

iframe {
    width: 99%;
    height: 99%;
}
</style>
