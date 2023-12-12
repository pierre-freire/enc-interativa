<template>
  <nav class="navbar">
    <button class="mobile-menu" :class="{ open: menuOpen }" @click="changeMenuOpen(!menuOpen)" type="button" aria-label="Menu">
      <img class="mobile-menu--icon" src="../assets/menu-icon.webp" alt="icon do menu mobile" />
    </button>
    <ul class="list" :class="{ open: menuOpen }">
      <li class="list-item"><a class="list-item__link" href="#hero">home</a></li>
      <li class="list-item"><a class="list-item__link" href="#participate">como participar</a></li>
      <li class="list-item"><a class="list-item__link" href="#awards_list">prêmios</a></li>
      <li class="list-item"><a class="list-item__link" href="#products">produtos participantes</a></li>
      <li class="list-item"><a class="list-item__link" href="/">receitas</a></li>
      <li class="list-item"><a class="list-item__link" href="/">pílulas nba</a></li>
      <li class="list-item"><a class="list-item__link" href="/">ganhadores</a></li>
      <li class="list-item user">
        <button class="list-item__button" type="button">olá, ana<span class="triangle"></span></button>
        <ul class="user-info">
          <li class="info-link">Perfil</li>
          <li class="info-link">Cupons</li>
          <li class="info-link">Sair</li>
        </ul>
      </li>
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
  justify-content: flex-end;
  font-family: Brandon;
  background-color: #FACC1f;
  position: relative;
}

.mobile-menu {
  background: none;
  border: none;
  transform: rotate(180deg);
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
  text-transform: uppercase;
  max-width: 180px;
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
  text-decoration: none;
  text-wrap: wrap;
}

.list-item__button {
  padding: 8px 16px;
  height: 100%;
  display: flex;
  align-items: center;
  box-sizing: border-box;
  background: none;
  border: none;
  color: #074A75;
  font-size: var(--big-text);
  text-wrap: nowrap;
  text-decoration: none;
  font-family: Brandon;
  text-transform: uppercase;
}

.list-item__link:hover,
.list-item__button:hover {
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
  transform: rotate(180deg);
  transition: transform 0.5s ease;
}

.list-item__button:hover .triangle {
  border-color: transparent transparent #FACC1f transparent;
  transform: rotate(0deg);
}

.user {
  position: relative;
}

.user-info {
  position: absolute;
  right: 0;
  left: 0;
  top: 100%;
  background-color: #FACC1f;
  color: #074A75;
  font-size: var(--big-text);
  transform: scaleY(0);
  transform-origin: top;
  transition: all 0.4s ease;
}

.user:hover .triangle {
  transform: rotate(0deg);
}

.user:hover .user-info{
  transform: scaleY(1);
}

.info-link {
  padding: 4px;
}

.info-link:hover {
  background-color: #074A75;
  color: #FACC1f;
  cursor: pointer;
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
    position: initial;
    background: none;
    transform: scaleY(1);
  }
}
</style>