<template>
    <input type="text" :placeholder="text" class="border text-base font-normal text-[#161616] w-full pl-3 h-[52px] rounded-md bg-gray-100 focus:border-gray-300 focus:border-1.5 outline-none">
</template>

<script>
    export default {
        name: "ShortAnswer",
        props:{
            text: String
        }
    }
</script>

<style lang="scss" scoped>

</style>