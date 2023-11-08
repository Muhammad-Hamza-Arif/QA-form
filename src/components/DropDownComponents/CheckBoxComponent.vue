<template>
    <input type="checkbox" id="checkbox" class="h-4 w-4 ml-1">
    <input
      type="text"
      :placeholder="placeholder"
      v-model="text"
      id="question"
      class="border ml-2 text-base font-normal text-[#161616] w-[211px] pl-3 h-[52px] rounded-md outline-none focus:border-gray-400"
    />
    <button class="ml-3">
        <img src="../../assets/icons8-cross-16.png" alt="cross-icon" color="" >
    </button>
</template>

<script>
    export default {
        name: "CheckBoxComponent",
        props:{
            placeholder: String
        }
    }
</script>

<style lang="scss" scoped>

</style>