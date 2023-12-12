<template>
  <section class="video">
    <h2 class="title">
      dos dribles e enterradas memoráveis ao zerar do cronômetro,<br/>
      <span class="second-line">
        cada hora h da nba fica ainda mais saborosa com hellman's
      </span>
    </h2>
    <h3 class="sub-title">assista ao filme abaixo:</h3>
    <iframe class='player' width="100%" height="480" src="https://www.youtube.com/embed/KAIR1_wOJvg?si=YgG-Y8LUOX-DKOMD" title="video promocional"></iframe>
  </section>
</template>

<script>
export default {
  name: 'VideoSection',
}
</script>

<style scoped>
.video {
  color: white;
  padding: 48px 16px;
}

.title {
  line-height: 1.2;
  text-transform: uppercase;
  font-size: var(--normal-title);
  font-family: Brandon Med;
}

.second-line {
  font-family: Brandon;
}

.sub-title {
  font-size: var(--big-title);
  text-transform: uppercase;
  margin-bottom: 36px;
}

.player {
  max-width: 860px;
}
</style>
