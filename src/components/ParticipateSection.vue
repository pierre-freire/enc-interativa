<template>
  <section class="participate">
    <h2 class="title">COMO PARTICIPAR</h2>
    <div class="phases">
      <img src="../assets/passo-1.png" alt="passo 1 para participar" />
      <img src="../assets/passo-2.png" alt="passo 2 para participar" />
      <img src="../assets/passo-3.png" alt="passo 3 para participar" />
      <img src="../assets/passo-4.png" alt="passo 4 para participar" />
    </div>
    <div>
      <img class="img" src="../assets/extra-1.png" alt="prêmio para 1 cesta" />
      <img class="img" src="../assets/extra-2.png" alt="prêmio para 3 cestas" />
      <img class="img" src="../assets/extra-3.png" alt="prêmio para 2 cestas extras" />
    </div>
    <img class="img" src="../assets/extra-4.png" alt="prêmio para 1 cesta em sp capital" />
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
  font-size: 36px;
  font-family: Latino;
  border-bottom: 3px solid;
  display: inline-flex;
  padding: 4px;
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
