<template>
    <div>
        <HeaderSearch @emitUrlOrgin="getUrlOrgin" ref="headerSearchrl"></HeaderSearch>
        <section class="m-content">
            <iframe :src="url" frameborder="0" ref="iframe"></iframe>
        </section>
    </div>
</template>

<script setup lang="ts">
import HeaderSearch from './components/HeaderSearch.vue';
import { ref } from 'vue';

let url = ref('');

const getUrlOrgin = (data:string) =>{
    url.value = data;
}
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
