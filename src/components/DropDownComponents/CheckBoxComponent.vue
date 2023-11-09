<template>
  <input type="checkbox" :id="id" class="h-4 w-4 ml-1" />
  <input
    type="text"
    :id="id"
    :placeholder="placeholder"
    class="border ml-2 text-base font-normal text-[#161616] w-[211px] pl-3 h-[45px] rounded-md outline-none focus:border-gray-400"
  />
  <button class="ml-4" @click="checkBoxId">
    <svg
      width="16"
      height="16"
      viewBox="0 0 16 16"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M12.8854 1.77563L13.9139 2.80415L9.07753 7.63963L14.0133 12.5751L12.9848 13.6036L8.04917 8.668L3.11446 13.6036L2.08594 12.5751L7.02081 7.63963L2.18535 2.80415L3.21387 1.77563L8.04917 6.61127L12.8854 1.77563Z"
        fill="#414141"
      />
    </svg>
  </button>
</template>
<script>

export default {
  name: "CheckBoxComponent",
  components: {},
  props: {
    placeholder: String,
    id: Number,
  },
  methods: {
    checkBoxId() {
      console.log("id ", this.id);
      this.$emit("sendId", this.id);
    },
  },
};
</script>

<style lang="scss" scoped></style>
