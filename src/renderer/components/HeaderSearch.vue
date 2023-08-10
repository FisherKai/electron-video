<template>
    <div>
        <el-input v-model="urlText" placeholder="Please input">
            <template #prepend>
                    <el-button @click="changePre">{{prependText}}</el-button>
</template>

<template #append>
    <el-button @click="searchOrgin">
        🔍</el-button>
</template>
    </el-input>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const urlText = ref('')
const prependText = ref('http://')

const searchOrgin = () => {
    const url = `${prependText.value}${urlText.value}`
}

const changePre = () => {
    if(prependText.value === 'http://'){
        prependText.value = 'https://'
        return
    }
    if(prependText.value === 'https://'){
        prependText.value = 'http://'
        return
    }
}
</script>

<style>

</style>