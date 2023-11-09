<template>
    <div class="w-full">
        <div class="p-5">
      <InputField placeholder="What do you want to ask?"/>
      <AnswerField :options="options" class="mt-4"/>
    </div>
    </div>
</template>

<script>
import InputField from '../components/InputField.vue';
import AnswerField from '../components/AnswerField.vue';

    export default {
    name: "QAComponent",
    components: { InputField, AnswerField },
    data(){
    return{
      options:["Short Answer","Paragraph","Multiple Choice","CheckBox","DropDown"]
    }
  }
}
</script>

<style lang="scss" scoped>

</style>