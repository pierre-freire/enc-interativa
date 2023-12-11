<template>
  <section class="awards-container">
    <div class='awards'>
      <img class="awards-img" src="../assets/premios.webp" alt="imagem dos prêmios" />
    </div>
  </section>
</template>

<script>
export default {
  name: 'AwardsSection',
}
</script>

<style scoped>
.awards {
  margin: 16px;
  padding: 36px 16px;
  border-radius: 36px;
  border: 4px solid #074A75;
  background-color: #122641;
  box-shadow: 0px 0px 0px 16px #122641;
  position: relative;
  z-index: 1;
}

.awards-container {
  position: relative;
}

.awards-container::before {
  content: '';
  position: absolute;
  top: -16px;
  left: 0;
  right: 0;
  height: 60px;
  background-image: url('../assets/bg-azul.webp');
}

.awards-img {
  max-width: 100%;
}
</style>
