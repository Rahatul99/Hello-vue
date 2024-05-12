<template>
  <div>
    <Greet name="abc" heroName="superman" />
    <Greet name="def" heroName="superMan" />
    <Greet name="ghi" heroName="BatMan" />
    <Greet :name="name" :heroName="channel" />
  </div>
</template>

<script>
import Greet from "./components/Greet.vue";

export default {
  name: "App",
  components: {
    Greet,
  },
  data() {
    return {
      name: "Dynamic",
      channel: "Props",
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
