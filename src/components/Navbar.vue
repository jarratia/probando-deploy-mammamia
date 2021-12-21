<template>
  <div class="navbar d-flex justify-content-between text-white py-3">
    <div class="container">
      <router-link to="/">
        <div class="d-flex">
          <h4 class="mb-0">&#127829;</h4>
          <h4 class="mx-1 mb-0">Pizzería Mamma Mia!</h4>
        </div>
      </router-link>

      <router-link to="/carrito">
        <div>
          <h4 class="mb-0">&#128722; $ {{formatNumber(total)}}</h4>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex';
import utils from "@/utils/functions";
const { formatNumber } = utils;
export default {
  name: "Navbar",
  props: {
    msg: String,
  },
  computed: {
    ...mapGetters([ "total"]),
  },
  methods:{
    formatNumber
  }
};
</script>


<style scoped>
.navbar {
  background: #17a2b8;
}
</style>
