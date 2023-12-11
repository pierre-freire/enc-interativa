<template>
  <footer class="footer">
    <div class="laco-container">
      <img class="laco-logo" src="../assets/laco.webp" alt="logo da laco" loading="lazy" />
    </div>
    <div class="doubts-rules">
      <a class="doubts" href="/">DÚVIDAS</a>
      <a class="rules" href="/">REGULAMENTO</a>
    </div>
    <ul class="social-networks">
      <li><img src="../assets/redes-twitter.webp" alt="logo do twitter" loading="lazy" /></li>
      <li><img src="../assets/redes-facebook.webp" alt="logo do facebook" loading="lazy" /></li>
      <li><img src="../assets/redes-instagram.webp" alt="logo do instagram" loading="lazy" /></li>
      <li><img src="../assets/redes-yt.webp" alt="logo do youtube" loading="lazy" /></li>
    </ul>
    <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum id dolor id turpis ultrices pharetra ac quis ligula. Mauris ut ante vel erat congue suscipit. In in aliquet enim, vitae tincidunt velit. Donec pellentesque commodo tincidunt. Pellentesque ut magna eget leo semper condimentum et volutpat nisi. Sed suscipit dui in nisl pretium, vitae egestas metus rhoncus. In</p>
    <img src="../assets/logo-unilever.webp" alt="logo unilever" loading="lazy">
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style scoped>
.footer {
  padding: 36px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.laco-container {
  position: relative;
  width: 100%;
}

.laco-container::before {
  content: '';
  height: 50%;
  width: 100%;
  border-top: 2px solid white;
  position: absolute;
  display: block;
  bottom: 0;
}

.laco-logo {
  position: relative;
  z-index: 1;
}

.doubts-rules {
  color: white;
  display: flex;
  gap: 48px;
  justify-content: center;
  margin: 24px 0;
  font-size: var(--big-text);
  flex-wrap: wrap;
}

.doubts-rules > a {
  cursor: pointer ;
  text-decoration: none;
  color: white;
}

.social-networks {
  display: flex;
  justify-content: space-around;
  width: 100%;
  max-width: 480px;
  margin: 24px 0;
}

.description {
  color: white;
  margin: 24px 0;
  max-width: 1400px;
}
</style>