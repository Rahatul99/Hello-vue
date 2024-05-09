<script>
export default {
  name: "App",
  data() {
    return {
      name: "Rahat",
      count: 0,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
    increment(num) {
      this.count += num;
    },
    decrement(num) {
      this.count -= num;
    },
    changeName(event) {
      this.name = "Batman";
      console.log(event);
    },
  },
};
</script>

<template>
  <div>
    <h1>{{ name }}</h1>
    <button @:mouseover="changeName">Click me</button>

    <h1>{{ count }}</h1>
    <button @:click="increment(5)">Increment</button>
    <button @:click="decrement(5)">Decrement</button>
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
