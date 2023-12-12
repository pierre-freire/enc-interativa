<template>
	<section class="hero" id="hero">
		<div class="hero-container">
			<h1 class="title">hellmann's hora h da nba</h1>
			<img class="pote de hellmann's que representa a promoção " src="../assets/logo-promo.webp" alt="logomarca da hellmann's" />
			<div class="hero-container__right-container">
				<img class="logo unilever-logo" src="../assets/logo-unilever.webp" alt="logomarca da unilever" />
				<LinkComponent label='PARTICIPE' />
				<img class="logo products" src="../assets/produtos-home.webp" alt="pratos e bowls com escudos dos times e tábua com desenho de quadra de basquete" />
			</div>
		</div>
	</section>
</template>

<script>
import LinkComponent from './LinkComponent.vue';

	export default {
		name: "HeroSection",
		components: {
			LinkComponent
		}
	};
</script>

<style scoped>
.hero {
	padding: 24px 24px 0;
	background-image: url('../assets/bg-azul.webp');
	display: flex;
	justify-content: center;
	width: 100%;
	box-sizing: border-box;
}

.hero-container__right-container {
	display: grid;
	grid-template-rows: 90px 180px 1fr;
}

.title {
	position: absolute;
	text-transform: uppercase;
	width: 1px;
	height: 1px;
	padding: 0;
	margin: -1px;
	overflow: hidden;
	clip: rect(0, 0, 0, 0);
	white-space: nowrap;
	border-width: 0;
}

.logo {
	max-width: 100%;
	align-self: end;
}

.unilever-logo {
	width: 90px;
	justify-self: flex-end;
	max-height: 100%;
	object-fit: contain;
}

.link-container {
	display: flex;
	align-items: center;
	justify-content: center;
}

.link-container__button {
  color: #074A75;
	background-color: #FACC1f;
	font-family: Brandon;
	font-size: var(--normal-title);
	padding: 16px 40px;
	border-radius: 60px;
	cursor: pointer;
	border: none;
	box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6);
}

.products {
	align-self: end;
	max-width: 100%;
}

@media (min-width: 640px) {
	.hero-container {
		max-width: 1600px;
		display: grid;
		grid-template-columns: 1fr 1fr;
	}	
}
</style>
