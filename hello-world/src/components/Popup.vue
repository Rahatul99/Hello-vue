<template>
  <div>
    <h3>PopUp component</h3>
    <input type="text" v-model="name" />
    <button @click="$emit('close', name)">Close popup</button>
  </div>
</template>

<script>
export default {
  name: "Popup",
  emits: {
    close: (name) => {
      if (name) {
        return true;
      } else {
        return false;
      }
    },
  },
  data() {
    return { name: "" };
  },
};
</script>

<style lang="scss" scoped></style>
