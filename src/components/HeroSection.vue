<template>
	<section class="hero">
		<div class="hero-container">
			<img class="logo" src="../assets/logo-promo.png" alt="hellmans logo" />
			<div class="hero-container__right-container">
				<img class="logo unilever-logo" src="../assets/logo-unilever.png" alt="unilever logo" />
				<div class="button-container">
					<button class="button-container__button">PARTICIPE</button>
				</div>
				<img class="logo products" src="../assets/produtos-home.png" alt="proodutos da promoção" />
			</div>
		</div>
	</section>
</template>

<script>
	export default {
		name: "HeroSection",
	};
</script>

<style scoped>
.hero {
	padding: 24px;
	background-image: url('../assets/bg-azul.jpg');
	display: flex;
	justify-content: center;
	width: 100%;
	box-sizing: border-box;
}

.hero-container {
	max-width: 1600px;
	display: flex;
}

.logo {
	object-fit: none;
}

.hero-container__right-container {
	display: grid;
	grid-template-rows: 90px 180px 1fr;
}

.unilever-logo {
	width: 90px;
	justify-self: end;
}

.button-container {
	display: flex;
	align-items: center;
	justify-content: center;
}

.button-container__button {
  color: #074A75;
	background-color: #FACC1f;
	font-family: Brandon;
	font-size: 40px;
	padding: 16px 40px;
	border-radius: 60px;
	cursor: pointer;
	border: none;
	box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6);
}

.products {
	align-self: end;
}
</style>
