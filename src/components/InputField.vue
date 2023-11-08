<template>
  <div class="h-[72px]">
    <label for="question" class="block text-xs font-normal mb-1">Question</label>
    <input
      type="text"
      :placeholder="placeholder"
      v-model="text"
      id="question"
      class="border text-base font-normal text-[#161616] w-[271px] pl-3 h-[52px] rounded-md"
    />
  </div>
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
