<script>
export default {
  name: "App",
  data(){
    return{
      headingId: "heading",
      isDisabled: false,
      status: "danger"
    }
  }
}
</script>

<template>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h1 class="underline">underline text</h1>
  <!-- dynamic class property is below -->
  <h2 v-bind:class="status">Status</h2>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
.danger{
  color: red;
}
.underline{
  text-decoration: underline ;
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
