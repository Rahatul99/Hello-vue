<template>
  <ClickCounter />
  <HoverCounter />
</template>

<script>
import ClickCounter from "./components/ClickCounter.vue";
import HoverCounter from "./components/HoverCounter.vue";

export default {
  name: "App",
  components: {
    ClickCounter,
    HoverCounter,
  },
  data() {
    return {};
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
h4 {
  color: red;
}
</style>
