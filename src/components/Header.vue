<template>
  <div
    class="header d-flex flex-column justify-content-center text-white text-center"
  >
    <h1>¡Pizzería mamma mia</h1>
    <h6>¡Somos el mejor país de chile!</h6>
    <hr class="w-75 mx-auto" />
  </div>
</template>

<style scoped>
.header {
  background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url("~@/assets/Header.jpg");
  background-size: cover;
  height: 30vh;
}

h1 {
  font-size: 50px;
}

h6 {
  font-size: 20px;
}
</style>

<script>
export default {
  name: "Header",
};
</script>
