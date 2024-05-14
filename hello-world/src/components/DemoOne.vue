<template>
  <h2>{{ name }}</h2>
</template>

<script>
import { ref } from "vue";
export default {
  name: "DemoOne",
  setup() {
    const name = ref("Vishwas");

    setTimeout(() => {
      name.value = "Codevolution";
    }, 2000);
    return {
      name,
    };
  },

  // it also works
  // setup() {
  //   let state = reactive({ name: "Vishwas" });

  //   setTimeout(() => {
  //     state.name = "Codevolution";
  //   }, 2000);
  //   return {
  //     state,
  //   };
  // },

  //but below it is did'nt works
  // setup() {
  //   let name =  "Vishwas";

  //   setTimeout(() => {
  //     name = "Codevolution";
  //   }, 2000);
  //   return {
  //     name,
  //   };
  // },
};
</script>

<style scoped></style>
