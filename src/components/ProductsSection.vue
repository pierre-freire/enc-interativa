<template>
  <section class="products">
    <h2 class="title">PRODUTOS PARTICIPANTES</h2>
    <p class="description">TODOS OS SQUEEZES DA LINHA HELLMANN'S</p>
    <img class="products-img" src="../assets/produtos-home.png" alt="proodutos da promoção" />
  </section>
</template>

<script>
export default {
  name: 'ProductsSection'
}
</script>

<style scoped>
.products {
  margin: 16px;
  padding: 36px 16px;
  border-radius: 36px;
  border: 4px solid #074A75;
  background-color: #122641;
  box-shadow: 0px 0px 0px 16px #122641;
  color: white;
}

.title {
  font-size: 48px;
  font-family: Latino;
  border-bottom: 4px solid white;
  display: inline-block;
  margin-bottom: 24px;
  padding: 8px 0;
}

.description {
  font-size: 36px;
}

.products-img {
  margin-top: 36px;
  margin-bottom: -59px;
  width: 80%;
}
</style>
