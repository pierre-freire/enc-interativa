<template>
  <nav class="navbar">
    <ul class="list">
      <li class="list-item"><a class="list-item__link">HOME</a></li>
      <li class="list-item"><a class="list-item__link">COMO<br/>PARTICIPAR</a></li>
      <li class="list-item"><a class="list-item__link">PRÊMIOS</a></li>
      <li class="list-item"><a class="list-item__link">PRODUTOS<br/>PARTICIPANTES</a></li>
      <li class="list-item"><a class="list-item__link">RECEITAS</a></li>
      <li class="list-item"><a class="list-item__link">PÍLULAS NBA</a></li>
      <li class="list-item"><a class="list-item__link">GANHADORES</a></li>
      <li class="list-item"><a class="list-item__link">OLÁ, ANA</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavbarComponent'
}
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: center;
  font-family: Brandon;
  background-color: #FACC1f;
}

.list {
  display: flex;
  max-width: 1600px;
}

.list-item {
  display: flex;
  align-items: center;
}

.list-item__link {
  padding: 8px 16px;
  height: 100%;
  display: flex;
  align-items: center;
  box-sizing: border-box;
  color: #074A75;
  font-size: 20px;
  text-wrap: nowrap;
}

.list-item__link:hover {
  color: #FACC1f;
  background-color: #074A75;
  cursor: pointer;
}
</style>