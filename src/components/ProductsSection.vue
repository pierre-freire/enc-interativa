<template>
  <section class="products-container" id="products">
    <div class="products">
      <h2 class="title">produtos participantes</h2>
      <p class="description">todos os squeezes da linha hellmann's</p>
      <img class="products-img" src="../assets/produtos-home.webp" alt="potes de hellman's referentes à promoção" loading="lazy" />
    </div>
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
  position: relative;
}

.products-container {
  position: relative;
  width: 100%;
}

.products-container::before {
  content: '';
  position: absolute;
  bottom: -36px;
  left: 0;
  right: 0;
  height: 60px;
  background-image: url('../assets/bg-azul.webp');
}

.title,
.description {
  text-transform: uppercase;
}
.title {
  font-size: var(--big-title);
  font-family: Latino;
  border-bottom: 4px solid white;
  display: inline-block;
  margin-bottom: 24px;
  padding: 8px 0;
}

.description {
  font-size: var(--normal-title);
}

.products-img {
  margin-top: 36px;
  margin-bottom: -59px;
  width: 80%;
}
</style>
