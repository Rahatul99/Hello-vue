<template>
  <div>
    <h2>option api: {{ o_firstName }}</h2>
    <h2>Composition api: {{ c_firstName }}</h2>
    <h2>{{ greet }}</h2>

    <h2>Reactive composition: {{ reactiveHero }}</h2>
  </div>
</template>

<script>
import { reactive, ref } from "vue";
export default {
  name: "Data",
  setup() {
    const c_firstName = ref("Clark");
    c_firstName.value = "Diana";
    const greet = `Hello ${c_firstName.value}`;

    const state = reactive({
      firstName: "Princess",
      lastName: "Diana",
      heroName: "Wonder woman",
    });

    // const isLoggedIn = ref(false);  in the below isLoggedInReactive is the replace of it
    // const isLoggedInReactive = reactive({
    //   value: false,
    // });

    const reactiveHero = `Hello ${state.firstName} ${state.lastName} and ${state.heroName}`;
    return {
      c_firstName,
      greet,
      reactiveHero,
    };
  },
  data() {
    return {
      o_firstName: "Bruce",
    };
  },
};
</script>

<style lang="scss" scoped></style>
