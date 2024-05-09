<script>
export default {
  name: "App",
  data(){
    return{
      num: -1,
      display: true,
      showElement: false
    }
  }
}
</script>

<template>
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">This is the negative number</h2>
  <h2 v-else>The number is not zero </h2>

  <template v-if="display">
    <!-- <div>Hello world</div>
    <div>Hi world</div>
    <div>Greetings world</div> -->
    <br>

    <h2 v-show="showElement">Using v-show</h2>
    <h2 v-if="showElement">Using v-if</h2>
  </template>
</template>

<style scoped>  
header {
  line-height: 1.5;
}

.new{
  color: green;
}
.sold-out{
  color: red
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
.promoted{
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
