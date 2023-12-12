<template>
  <section class="buy">
    <h2 class="title">compre agora e participe</h2>
    <ul class="buy-list">
      <li class="buy-option">
        <img class="buy-option__img" src="../assets/pda.webp" alt="logomarca do pão de açucar" loading="lazy" />
        <a class="link" href="/">gpa</a>
      </li>
      <li class="buy-option">
        <img class="buy-option__img" src="../assets/carrefour.webp" alt="logomarca do carrefour" loading="lazy" />
        <a class="link" href="/">carrefour</a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'BuySection'
}
</script>

<style scoped>
.buy {
  padding: 24px;
  background-image: url('../assets//bg-azul.webp');
}

.title {
  color: white;
  font-size: var(--normal-title);
  font-family: Latino;
  border-bottom: 4px solid white;
  display: inline-block ;
  padding-bottom: 8px;
  text-transform: uppercase;
}

.buy-list {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 24px;
  padding: 24px;
}

.buy-option {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 24px;
  text-transform: uppercase;
}

.buy-option__img {
  width: 156px;
}

.link {
  color: #074A75;
	background-color: #FACC1f;
	font-family: Brandon;
	font-size: var(--normal-text);
	padding: 16px 40px;
	border-radius: 60px;
	cursor: pointer;
	border: none;
	box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6);
  min-width: 80px;
  text-decoration: none;
}
</style>