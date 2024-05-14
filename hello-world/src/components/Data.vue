<template>
  <div>
    <h2>option api: {{ o_firstName }}</h2>
    <h2>Composition api: {{ c_firstName }}</h2>
    <h2>{{ greet }}</h2>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Data",
  setup() {
    const c_firstName = ref("Clark");
    c_firstName.value = "Diana";
    const greet = `Hello ${c_firstName.value}`;
    return {
      c_firstName,
      greet,
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
