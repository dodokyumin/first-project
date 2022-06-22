<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>


  <!-- <span v-for="alias in items" :key="alias.name">
    <span>{{ alias.name }}</span> : <span>{{ alias.age }}</span><br>
  </span> -->
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
  },
  data() {
      return {
      items: [
        { name: "john", age: 31 },
        { name: "steve", age: 32 },
        { name: "jake", age: 30 }
      ]
    }
  }
};
</script>
