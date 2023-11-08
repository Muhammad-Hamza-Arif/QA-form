<template>
  <div class="mx-auto w-96">
    <!-- <InputField placeholder="What do you want ask? "/>
  <hr class="w-[271px] my-4"> -->
    <NavBar :options="options"/>
  </div>
</template>

<script>
import InputField from "./components/InputField.vue";
import NavBar from "./components/AnswerField.vue";
export default {
  name: "App",
  components: {
    NavBar,
    InputField,
  },
  data(){
    return{
      options:["Short Answer","Paragraph","Multiple Choice","CheckBox","DropDown"]
    }
  }
};
</script>

<style lang="scss" scoped></style>
