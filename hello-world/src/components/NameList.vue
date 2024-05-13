<template>
  <div>
    <h3 v-for="name in names" :key="name.firstName">
      <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
    </h3>
  </div>
</template>

<script>
export default {
  name: "NameList",
  data() {
    return {
      names: [
        {
          firstName: "Bruch",
          lastName: "Wayne",
        },
        {
          firstName: "Clark",
          lastName: "Kent",
        },
        {
          firstName: "Princess",
          lastName: "Diana",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
