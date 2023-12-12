<template>
  <section class="participate" id="participate">
    <h2 class="title">como participar</h2>
    <div class="phases">
      <img src="../assets/passo-1.webp" alt="passo 1 para participar" loading="lazy" />
      <img src="../assets/passo-2.webp" alt="passo 2 para participar" loading="lazy" />
      <img src="../assets/passo-3.webp" alt="passo 3 para participar" loading="lazy" />
      <img src="../assets/passo-4.webp" alt="passo 4 para participar" loading="lazy" />
    </div>
    <div>
      <img class="img" src="../assets/extra-1.webp" alt="pote de hellman's, prêmio para 1 cesta" loading="lazy" />
      <img class="img" src="../assets/extra-2.webp" alt="pote de hellman's supreme, prêmio para 3 cestas" loading="lazy" />
      <img class="img" src="../assets/extra-3.webp" alt="pacotes de ruffles, prêmio para 2 cestas extras" loading="lazy" />
    </div>
    <img class="img" src="../assets/extra-4.webp" alt="prêmio para 1 cesta em são paulo capital" loading="lazy" />
    <LinkComponent label='PARTICIPE' />
  </section>
</template>

<script>
import LinkComponent from './LinkComponent.vue';

export default {
  name: 'ParticipateSection',
  components: {
    LinkComponent
  }
}
</script>

<style scoped>
.participate {
  padding: 36px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.title {
  color: white;
  font-size: var(--normal-title);
  font-family: Latino;
  border-bottom: 3px solid;
  display: inline-flex;
  padding: 4px;
  text-transform: uppercase;
}

.phases {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 32px;
  margin: 36px 0;
}

.img {
  max-width: 100%;
}
</style>
