<template>
    <div>
        <el-input v-model="urlText" placeholder="Please input">
            <template #prepend>
                <el-button @click="changePre">{{ prependText }}</el-button>
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

const emit = defineEmits(['emitUrlOrgin'])

const urlText = ref('')
const prependText = ref('http://')

const searchOrgin = () => {
    const url = urlText.value.includes("http://") || urlText.value.includes("https://") ? `${urlText.value}` : `${prependText.value}${urlText.value}`;
    console.log(url);
    emit('emitUrlOrgin', url);
}

const changePre = () => {
    if (prependText.value === 'http://') {
        prependText.value = 'https://'
        return
    }
    if (prependText.value === 'https://') {
        prependText.value = 'http://'
        return
    }
}
</script>

<style></style>