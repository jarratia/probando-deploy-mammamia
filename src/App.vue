<template>
  <div id="app">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import { mapActions } from "vuex";
export default {
  mounted() {
    this.get_Pizzas();
  },
  methods: {
    ...mapActions(["get_Pizzas"]),
  },
  components: {
    Navbar,
  },
};
</script>

<style>
a,
a:hover {
  text-decoration: none;
  color: white;
}

ul {
  list-style: none;
}
</style>
