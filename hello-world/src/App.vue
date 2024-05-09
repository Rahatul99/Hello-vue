<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Bruce", "Clark", "Diana"],
      fullName: [
        { first: "don", last: "jon" },
        { first: "tom", last: "jerry" },
        { first: "cristiano", last: "ronaldo" },
      ],
      players: ["Alvas", "Tony", "Miller", "Rodrigo"],
      actors: [
        {
          name: "Leonardo DiCaprio",
          movies: ["Inception", "The Wolf of Wall Street"],
        },
        { names: "Tom Hanks", movie: ["Forrest Gump", "Cast Away"] },
        {
          name: "Meryl Streep",
          movies: ["The Devil Wears Prada", "Sophie's Choice"],
        },
        { name: "Denzel Washington", movie: ["Training Day", "Glory"] },
        {
          name: "Scarlett Johansson",
          movies: ["Lost in Translation", "The Avengers"],
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <!-- <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
    <h2 v-for="(name, index) in fullName" :key="name.first">
      {{ index }}{{ name.first }} {{ name.last }}
    </h2>

    <h2 v-for="(actor, index) in actors" :key="actor.name">
      {{ index }} {{ actor.name }}
      <h3 v-for="movie in actor.movies" :key="movie">
        {{ index }} number {{ movie }}
      </h3>
    </h2> -->

    <h2 v-for="player in players" :key="player">
      <!-- {{ player }} -->
      <h3 v-if="player === 'Tony'">{{ player }}</h3>
    </h2>
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
