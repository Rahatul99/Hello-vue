<template>
  <h2>Volume tracker</h2>
  <h3>Current volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
  <input type="text" v-model="movie" />
  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />

  <div>
    <button @click="movieList.push('Iron-man')">Add movie</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0,
      movie: "Batman",
      movieInfo: {
        title: "",
        actor: "",
      },
      movieList: ["Batman", "Superman"],
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert(
          "Listening to high volume for long time may damage you hearing.."
        );
      }
    },
    // movie(newValue) {
    //   console.log("hello world", newValue);
    // },
    movie: {
      handler(newValue) {
        console.log("called the watch handler", newValue);
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue) {
        console.log("called the movieInfo", newValue.title, newValue.actor);
      },
      // immediate: true,  here is immediate dosen't works cause of it is a nested property and watchers dosen't work within the nested property
      deep: true,
    },
    movieList: {
      handler(newValue) {
        console.log(newValue, "movie list");
      },
      deep: true,
    },
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
