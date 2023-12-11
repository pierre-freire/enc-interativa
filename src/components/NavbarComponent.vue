<template>
  <nav class="navbar">
    <button class="mobile-menu" :class="{ open: menuOpen }" @click="changeMenuOpen(!menuOpen)" aria-label="Menu">
      <img class="mobile-menu--icon" src="../assets/menu-icon.webp" alt="mobile menu icon" />
    </button>
    <ul class="list" :class="{ open: menuOpen }">
      <li class="list-item"><a class="list-item__link" href="/">HOME</a></li>
      <li class="list-item"><a class="list-item__link" href="/">COMO<br/>PARTICIPAR</a></li>
      <li class="list-item"><a class="list-item__link" href="/">PRÊMIOS</a></li>
      <li class="list-item"><a class="list-item__link" href="/">PRODUTOS<br/>PARTICIPANTES</a></li>
      <li class="list-item"><a class="list-item__link" href="/">RECEITAS</a></li>
      <li class="list-item"><a class="list-item__link" href="/">PÍLULAS NBA</a></li>
      <li class="list-item"><a class="list-item__link" href="/">GANHADORES</a></li>
      <li class="list-item"><a class="list-item__link" href="/">OLÁ, ANA<span class="triangle"></span></a></li>
    </ul>
  </nav>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'NavbarComponent',
  setup() {
    const menuOpen = ref(false)

    function changeMenuOpen(param) {
      menuOpen.value = param
    }

    return{
      menuOpen,
      changeMenuOpen
    }
  }
}
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: end;
  font-family: Brandon;
  background-color: #FACC1f;
  position: relative;
}

.mobile-menu {
  background: none;
  border: none;
  transform: rotate(0);
  transition: all 0.5s ease;
}

.mobile-menu--icon {
  width: 48px;
  height: 48px;
}

.mobile-menu.open {
  transform: rotate(90deg);
}

.list {
  display: flex;
  transform: scaleY(0);
  transform-origin: top;
  position: absolute;
  flex-direction: column;
  top: calc(100% - 1px);
  width: 100%;
  background-color: #FACC1f;
  transition: all 0.5s ease;
  align-items: center;
}

.list.open {
  transform: scaleY(1);
  display: flex;
}

.list-item {
  display: flex;
  align-items: center;
  height: 100%;
}

.list-item__link {
  padding: 8px 16px;
  height: 100%;
  display: flex;
  align-items: center;
  box-sizing: border-box;
  color: #074A75;
  font-size: var(--big-text);
  text-wrap: nowrap;
  text-decoration: none;
}

.list-item__link:hover {
  color: #FACC1f;
  background-color: #074A75;
  cursor: pointer;
}

.triangle {
  width: 0px;
  height: 0px;
  margin-left: 8px;
  border-style: solid;
  border-width: 0 10px 15px 10px;
  border-color: transparent transparent #074A75 transparent;
  transform: rotate(0deg);
}

.list-item__link:hover .triangle {
  border-color: transparent transparent #FACC1f transparent;
  transform: rotate(180deg);
}

@media (min-width: 1280px) {
  .mobile-menu {
    display: none;
  }
  .navbar {
    justify-content: center;
  }
  .list {
    flex-direction: row;
    justify-content: center;
    max-width: 1600px;
    position: initial;
    background: none;
    transform: scaleY(1);
  }
}
</style>