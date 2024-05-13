<template>
  <div><h2>This tab C</h2></div>
  <input type="text" v-model="name" />
</template>

<script>
export default {
  name: "TabC",
  data() {
    return {
      name: "",
    };
  },
};
</script>

<style scoped></style>
