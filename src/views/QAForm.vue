<template>
  <NavBar />
  <div class="max-w-[712px] mx-auto">
    <div
      v-for="(item, i) in addQuestions"
      :key="i"
      class="border bg-white mt-8"
    >
      <QAFormComponent class="" />
      <div
        v-if="addQuestions.length > 1"
        class="h-[40px] flex items-center justify-between p-5 list-none"
      >
        <li>{{ i + 1 }} of {{ addQuestions.length }}</li>
        <button @click="deleteQuestion(i)">
          <svg
            width="12"
            height="14"
            viewBox="0 0 12 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M2.72736 4.09091V12.4545H9.27282V4.09091H10.3637V13.5455H1.63645V4.09091H2.72736ZM5.091 4.81534V11.3636H4.00009V4.81534H5.091ZM8.00009 4.81534V11.3636H6.90918V4.81534H8.00009ZM8.18191 0.45694L8.90918 1.91149H11.091V3.00239H0.90918V1.91149H3.091L3.81827 0.45694H8.18191Z"
              fill="#AE0000"
            />
          </svg>
        </button>
      </div>
    </div>
    <ButtonComponent
      buttonText="ADD QUESTION"
      @click="addQuestion"
      class="mt-8 w-full border h-[40px] text-xs font-bold text-[#AE0000]"
    />
    <ButtonComponent
      buttonText="SAVE & SHARE"
      class="w-full border h-[40px] text-xs font-bold text-white mt-4 bg-[#AE0000]"
    />
  </div>
</template>

<script>
import ButtonComponent from "../components/ButtonComponent.vue";
import NavBar from "../components/NavBar.vue";
import QAFormComponent from "../components/QAFormComponent.vue";
export default {
  name: "QAForm",
  components: {
    NavBar,
    QAFormComponent,
    ButtonComponent,
  },
  data() {
    return {
      addQuestions: [{}],
    };
  },
  methods: {
    addQuestion() {
      this.addQuestions.push({});
    },
    deleteQuestion(id){
        this.addQuestions.splice(id,1)
    }
  },
};
</script>

<style lang="scss" scoped></style>
