<template>
  <div>
    <h4>App component text</h4>
    <ChildStyles />
  </div>
</template>

<script>
import ChildStyles from "./components/ChildStyles.vue";

export default {
  name: "App",
  components: {
    ChildStyles,
  },
  data() {
    return {};
  },
  method: {},
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
h4 {
  color: red;
}
</style>
