<template>
  <section class="participate">
    <h2 class="title">COMO PARTICIPAR</h2>
    <div class="phases">
      <img src="../assets/passo-1.png" />
      <img src="../assets/passo-2.png" />
      <img src="../assets/passo-3.png" />
      <img src="../assets/passo-4.png" />
    </div>
    <div>
      <img src="../assets/extra-1.png" />
      <img src="../assets/extra-2.png" />
      <img src="../assets/extra-3.png" />
    </div>
    <img src="../assets/extra-4.png" />
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
  gap: 32px;
  margin: 36px 0;
}
</style>
