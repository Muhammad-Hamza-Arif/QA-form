<template>
  <div class="w-[271px]">
    <label for="answer" class="text-xs font-normal block mb-4">Answer</label>
    <div
      class="flex items-center justify-between border p-2.5 rounded-md w-full h-[40px] text-sm cursor-pointer"
      @click="toggleDropdownVisibility"
    >
      <div class="">
        {{ selectedOption || (selectedOption = options[0]) }}
      </div>
      <div>
        <svg
          width="20px"
          height="20px"
          viewBox="0 0 24.00 24.00"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
          stroke="#ff0000"
          stroke-width="0.00024000000000000003"
          transform="rotate(0)"
        >
          <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
          <g
            id="SVGRepo_tracerCarrier"
            stroke-linecap="round"
            stroke-linejoin="round"
          ></g>
          <g id="SVGRepo_iconCarrier">
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M12.7071 14.7071C12.3166 15.0976 11.6834 15.0976 11.2929 14.7071L6.29289 9.70711C5.90237 9.31658 5.90237 8.68342 6.29289 8.29289C6.68342 7.90237 7.31658 7.90237 7.70711 8.29289L12 12.5858L16.2929 8.29289C16.6834 7.90237 17.3166 7.90237 17.7071 8.29289C18.0976 8.68342 18.0976 9.31658 17.7071 9.70711L12.7071 14.7071Z"
              fill="#AE0000"
            ></path>
          </g>
        </svg>
      </div>
    </div>
    <div v-if="isDropDownVisible">
      <div
        v-for="item in options"
        :key="item"
        class="border text-xs flex items-center p-2.5 cursor-pointer"
        @click="toggleOptionSelect(item)"
      >
        {{ item }}
      </div>
    </div>
    <div v-if="selectedOption == 'Short Answer'" class="mt-2.5">
      <ShortAnswerComponent text="Short answer text"/>
    </div>
    <div v-if="selectedOption == 'Paragraph'" class="mt-2.5">
      <ParagraphComponent text="Long answer text"/>
    </div>
    <div v-if="selectedOption == 'CheckBox'" class="mt-4">
      <CheckBoxComponent placeholder="First Option"/>
    </div>
  </div>
</template>

<script>
import ShortAnswerComponent from "./DropDownComponents/ShortAnswerComponent.vue";
import ParagraphComponent from "./DropDownComponents/ParagraphComponent.vue";
import CheckBoxComponent from "./DropDownComponents/CheckBoxComponent.vue";
export default {
  name: "AnswerField",
  props: {
    options: Array,
  },
  components: {
    ShortAnswerComponent,
    ParagraphComponent,
    CheckBoxComponent
  },
  data() {
    return {
      selectedOption: "",
      isDropDownVisible: false,
    };
  },
  methods: {
    toggleOptionSelect(option) {
      this.selectedOption = option;
      this.isDropDownVisible = false;
    },
    toggleDropdownVisibility() {
      this.isDropDownVisible = !this.isDropDownVisible;
      if (this.isDropDownVisible) {
        document.addEventListener("click", this.closeDropdownOnOutsideClick);
      }
    },
    closeDropdownOnOutsideClick(event) {
      const dropdownElement = this.$el;
      if (!dropdownElement.contains(event.target)) {
        this.isDropDownVisible = false;
      }
    },
  },
};
</script>

<style lang="scss" scoped></style>
