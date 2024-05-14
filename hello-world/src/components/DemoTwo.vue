<template>
  <div>
    <h2>{{ state.firstName }} and {{ state.lastName }}</h2>
  </div>
</template>

<script>
import { reactive, toRefs } from "vue";

export default {
  name: "DemoTwo",
  setup() {
    const state = reactive({
      firstName: "Bruce",
      lastName: "Wayne",
    });

    setTimeout(() => {
      state.firstName = "Clark";
      state.lastName = "Kent";
    }, 2000);

    toRefs(state);

    return {
      state,
    };
  },
};
</script>

<style scoped></style>

<!-- <template>
  <div>
    <h2>{{ state.firstName }} and {{ state.lastName }}</h2>
    <h4>{{ fname }} {{ Iname }}</h4>
  </div>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "DemoTwo",
  setup() {
    const state = reactive({
      firstName: "Bruce",
      lastName: "Wayne",
    });
    setTimeout(() => {
      (state.firstName = "Clark"), (state.lastName = "Kent");
    }, 2000);
    return {
    //but it doesn't works 
      // firstName: state.firstName,
      // lastName: state.lastName,

      //it works 
      state,
    };
  },
  data() {
    return {
      fname: "Bruce",
      Iname: "Wayne",
    };
  },
};
</script>

<style lang="scss" scoped></style> -->
