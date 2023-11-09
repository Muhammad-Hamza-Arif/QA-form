<template>
    <button class=""> {{ buttonText }}</button>
</template>

<script>
    export default {
        name: "ButtonComponent",
        props:{
            buttonText: String,
        }
    }
</script>

<style lang="scss" scoped>

</style>