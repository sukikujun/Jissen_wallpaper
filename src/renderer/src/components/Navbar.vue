<script setup lang="ts">
import { Pic, SettingOne } from "@icon-park/vue-next";
</script>

<template>
    <main class="px-4 py-2 text-sm opacity-80 flex justify-between items-center drag">
        <section class="text-xs opacity-80">wallpaper</section>
        <section class="flex items-center justify-center gap-2">
            <pic class="cursor-pointer nodrag" theme="outline" size="20" fill="#333"
                @click="$router.push({ name: 'home' })" />
            <setting-one class="cursor-pointer nodrag" theme="outline" size="20" fill="#333"
                @click="$router.push({ name: 'setting' })" />
        </section>
    </main>
</template>

<style lang="scss" scoped></style>
