<script setup lang="ts">
import { ref } from "vue";

const img = ref<HTMLImageElement>()
const loading = ref(false)
const load = () => {
    // const loading = ElLoading.service({ fullscreen: true })
    loading.value = true
    img.value!.src = `http://localhost:3000?k=${Math.random()}`
    img.value!.addEventListener('load', () => {
        loading.value = false
    })
}

console.log(loading.value);

</script>

<template>
    <main class="">
        <!-- draggable:false 禁止拖动 -->
        <!-- <img src="@renderer/assets/imgs/bg.jpeg" class="aspect-video nodrag" draggable="false"> -->
        <div v-loading="loading" element-loading-background="rgba(255, 255, 255, 0.4)">
            <img ref="img" src="http://localhost:3000/wallpaper/pic4.png" class="aspect-video nodrag" draggable="false"
                @click="load">
        </div>
        <div
            class="cursor-pointer bg-gray-200 text-center py-3 m-3 rounded-lg hover:bg-gray-300 duration-500 opacity-80 shadow-sm nodrag">
            壁紙に設定する</div>
        <div class="mx-3 text-xs m  flex justify-between">
            <div class="">※鈍色聴</div>
            <div class="hover:font-bold cursor-pointer text-sm nodrag">ダウンロード</div>
        </div>

    </main>
</template>

<style lang="scss" scoped></style>
