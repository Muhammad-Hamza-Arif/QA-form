<template>
  <header class="bg-[#AE0000] text-white w-full h-[60px]">
    <ul class="list-none flex justify-between items-center px-6 py-4">
      <li class="">
        <img src="../assets/logo.svg" alt="logo" />
      </li>
      <li class="text-[22px]">New Questionnair</li>
      <li class="bg-custom-color">
        <ButtonComponent buttonText="LOG IN" class="p-2 text-xs"/>
      </li>
    </ul>
  </header>
</template>

<script>
import ButtonComponent from "../components/ButtonComponent.vue";

export default {
  name: "NavBar",
  components: { ButtonComponent },
};
</script>

<style></style>
