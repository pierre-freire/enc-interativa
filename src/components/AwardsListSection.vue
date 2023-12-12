<template>
  <section class="awards-list" id="awards_list">
    <h2 class="title">COMPRE, JUNTE E TROQUE</h2>

    <ul class="selector-container">
      <li><button class="selector-button" :class="{ active: isActive('plates') }" @click="setActiveAward('plates')">PRATOS</button></li>
      <li><button class="selector-button" :class="{ active: isActive('bowls') }" @click="setActiveAward('bowls')">BOWLS</button></li>
      <li><button class="selector-button" :class="{ active: isActive('board') }" @click="setActiveAward('board')">TÁBUA</button></li>
    </ul>

    <ul class="galery">
      <li class="galery-item" :class="{ active: isActive('plates') }">
        <picture>
          <source srcset="../assets/galeria-pratos.webp" media="(min-width: 640px)"/>
          <img srcset="../assets/galeria-pratos-mob.webp" class="awards-img" alt="pratos com escudo dos times de basquete participantes" loading="lazy" />
        </picture>
      </li>
      <li class="galery-item" :class="{ active: isActive('bowls') }">
        <picture>
          <source srcset="../assets/galeria-bowls.webp" media="(min-width: 640px)"/>
          <img src="../assets/galeria-bowls-mob.webp" class="awards-img" alt="bowls com escudo dos times de basquete participantes" loading="lazy" />
        </picture>
      </li>
      <li class="galery-item" :class="{ active: isActive('board') }">
        <picture>
          <source srcset="../assets/galeria-tabua.webp" media="(min-width: 640px)"/>
          <img src="../assets/galeria-tabua-mob.webp" class="awards-img" alt="tábua de carne com deseno de quadra de basquete" loading="lazy" />
        </picture>
      </li>
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
  font-size: var(--normal-title);
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
  padding: 4px 8px;
  border-radius: 36px;
  border: none;
  color: white;
  background: none;
  cursor: pointer;
  font-family: Brandon;
  font-size: var(--normal-text);
}

.selector-button.active {
  color: #074A75;
  background-color: #facc1f;
}

.galery {
  display: flex;
  justify-content: center;
}

.galery-item {
  transition: max-width 0.4s ease;
  max-width: 00%;
}

.galery-item.active {
  max-width: 100%;
}

.awards-img {
  max-width: 100%;
}

@media (min-width: 640px) {
  .selector-button {
  padding: 4px 24px;
}
}
</style>
