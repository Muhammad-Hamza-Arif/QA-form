<template>
  <label for="question" class="block text-xs font-normal mb-1">Question</label>
  <input
    type="text"
    :placeholder="placeholder"
    v-model="text"
    id="question"
    class="border mt-4 text-base font-normal text-[#161616] pl-3 rounded-md block w-full outline-none h-[52px]"
  />
</template>

<script>
export default {
  name: "InputField",
  props: {
    placeholder: String,
  },
  data() {
    return {
      text: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>
