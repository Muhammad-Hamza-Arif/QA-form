<template>
  <div class="bg-[#F5F5F1]">
    <!-- <InputField placeholder="What do you want ask? "/>
  <hr class="w-[271px] my-4"> -->
    <!-- <NavBar :options="options"/> -->
    <QAForm/>
  </div>
</template>

<script>
// import InputField from "./components/InputField.vue";
// import NavBar from "./components/AnswerField.vue";
import QAForm from './views/QAForm.vue';
export default {
  name: "App",
  components: {
    // NavBar,
    // InputField,
    QAForm
  },
  data(){
    return{
      options:["Short Answer","Paragraph","Multiple Choice","CheckBox","DropDown"]
    }
  }
};
</script>

<style lang="scss" scoped></style>
