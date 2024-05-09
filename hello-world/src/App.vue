<script>
export default {
  name: "App",
  data() {
    return {
      baseMultiplier: 5,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
  },
};
</script>

<template>
  <div>
    <!-- {{ 2 * 5 + 3 }}
    add method: {{ add(5, 5, 5) }} add method: {{ add(6, 6, 6) }} -->
    {{ multiply(2) }}
  </div>
</template>

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
