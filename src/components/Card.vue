<template>
  <div class="card w-100">
    <img class="card-img-top" :src="pizza.img" />
    <div class="card-body">
      <h4 class="card-title text-capitalize">{{ pizza.name }}</h4>
      <hr />
      <p class="card-text ">
        <b>Ingredientes:</b>
      </p>
      <ul class="m-0">
        <li
          class="text-capitalize w-75"
          v-for="(ingrediente, i) in pizza.ingredients"
          :key="i"
        >
          &#127829; {{ ingrediente }}
        </li>
      </ul>
    </div>
    <hr />
    <div class="card-body">
      <h2 class="text-center text-dark pb-3">
        $ {{ formatNumber(pizza.price) }}
      </h2>
      <div class="d-flex justify-content-around">
        <router-link :to="`/pizza/${pizza.id}`"
          ><button class="btn btn-info text-white">
            Ver Más &#128064;
          </button></router-link
        >
        <button class="btn btn-danger" @click="addToCart(pizza.id)">
          Añadir &#128722;
        </button>
      </div>
    </div>
  </div>
</template>
<script>
import utils from "@/utils/functions";
const { formatNumber } = utils;
import { mapActions } from "vuex";

export default {
  name: "Card",
  props: ["pizza"],
  methods: {
    formatNumber,
    ...mapActions(["addToCart"]),
  },
};
</script>
