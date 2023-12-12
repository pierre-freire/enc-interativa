<template>
  <div class="link-container">
    <a class="link-container__link" href="/" >{{label}}</a>
  </div>
</template>

<script>
export default {
  name: 'LinkComponent',
  props: {
    label: String,
    link: String
  }
}
</script>

<style scoped>
.link-container {
	display: flex;
	align-items: center;
	justify-content: center;
}

.link-container__link {
  color: #074A75;
	background-color: #FACC1f;
	font-family: Brandon;
	font-size: var(--normal-title);
	padding: 16px 40px;
	border-radius: 60px;
	cursor: pointer;
	border: none;
	box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6);
	text-decoration: none;
}
</style>