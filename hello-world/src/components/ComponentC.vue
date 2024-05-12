<template>
  <h2>Component C {{ userName }}</h2>
</template>

<script>
export default {
  name: "ComponentC",
  inject: ["userName"],
};
</script>

<style lang="scss" scoped></style>
