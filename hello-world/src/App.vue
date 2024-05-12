<template>
  <div>
    <h3>App component userName {{ name }}</h3>
    <ComponentC />
  </div>
</template>

<script>
import ComponentC from "./components/ComponentC.vue";

export default {
  name: "App",
  components: {
    ComponentC,
  },
  data() {
    return {
      name: "Rahatul Islam",
    };
  },
  provide() {
    return {
      userName: this.name,
    };
  },
};
</script>

<style scoped>
header {
  line-height: 1.5;
}

.new {
  color: green;
}
.sold-out {
  color: red;
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}
.danger {
  color: red;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
