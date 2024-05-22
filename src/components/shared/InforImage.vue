<script setup lang="ts">
const { note, title, des, redirect } = defineProps<{
    note: string
    title: string
    des: string
    redirect: string
}>()
</script>

<template>
    <div class="text-red-400 text-lg font-bold uppercase tracking-widest">{{ note }}</div>
    <div class="w-[583px] h-[142px] text-indigo-950 text-[50px] font-bold font-['Volkhov'] leading-[71.04px] mb-6">
        {{ title }}</div>
    <p v-if="des" class="w-[583px] h-[103px] text-black text-base font-normal font-['Poppins'] leading-relaxed">Et
        {{ des }}</p>
    <el-button v-if="des">View packages</el-button>
    <slot name="custom" />
</template>