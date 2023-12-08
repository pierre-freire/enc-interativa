<template>
  <section class="awards-list">
    <h2 class="title">COMPRE, JUNTE E TROQUE</h2>

    <ul class="selector-container">
      <li><button class="selector-button" :class="{ active: isActive('plates') }" @click="setActiveAward('plates')">PRATOS</button></li>
      <li><button class="selector-button" :class="{ active: isActive('bowls') }" @click="setActiveAward('bowls')">BOWLS</button></li>
      <li><button class="selector-button" :class="{ active: isActive('board') }" @click="setActiveAward('board')">TÁBUA</button></li>
    </ul>

    <ul class="galery">
      <li><img class="galery-item" :class="{ active: isActive('plates') }" src="../assets/galeria-pratos.png" /></li>
      <li><img class="galery-item" :class="{ active: isActive('bowls') }" src="../assets/galeria-bowls.png" /></li>
      <li><img class="galery-item" :class="{ active: isActive('board') }" src="../assets/galeria-tabua.png" /></li>
    </ul>
  </section>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'AwardsListSection',
  setup() {
    const activeAward = ref('plates')

    function setActiveAward(param) {
      activeAward.value = param
    }

    function isActive(param) {
      if(activeAward.value === param) {
        return true
      } else {
        return false
      }
    }

    return {
      activeAward,
      setActiveAward,
      isActive
    }
  }
}
</script>

<style scoped>
.awards-list {
  margin: 16px;
  padding: 36px 16px;
  border-radius: 36px;
  border: 4px solid #074A75;
  background-color: #122641;
  box-shadow: 0px 0px 0px 16px #122641;
}

.title {
  font-size: 36px;
  color: #facc1f;
  font-family: Brandon;
  margin-bottom: 24px;
}

.selector-container {
  display: inline-flex;
  justify-content: center;
  padding: 4px;
  background-color: #074A75;
  border-radius: 36px;
  gap: 8px;
}

.selector-button {
  padding: 4px 24px;
  border-radius: 36px;
  border: none;
  color: white;
  background: none;
  cursor: pointer;
  font-family: Brandon;
  font-size: 16px;
}

.selector-button.active {
  color: #074A75;
  background-color: #facc1f;
}

.galery-item {
  display: none;
}

.galery-item.active {
  display: initial;
}
</style>
