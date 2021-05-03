<template lang="pug">
header
  section.title-container
    h1 Shundroid
    h2
      | A student,
      br
      | A programmer
  Motiv
</template>

<script>
import Motiv from './Motiv.vue'

export default {
  components: {
    Motiv
  }
}
</script>

<style scoped>
header {
  text-align: left;
  height: 100vh;
  background-color: #212121;
  color: #f5f5f5;
}
.title-container {
  padding: 0 5vw;
  box-sizing: border-box;
  height: calc(100% - 200px);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}
.title-container h1 {
  font-family: 'Press Start 2P', cursive;
  margin: 0;
  font-size: 5vh;
}
.title-container h2 {
  font-family: 'Electrolize', serif;
  margin-left: 3vw;
  font-size: 3vh;
  font-weight: normal;
}
@media (max-aspect-ratio: 2/3) {
  .title-container h1 {
    font-family: 'Press Start 2P', cursive;
    margin: 0;
    font-size: 7.5vw;
  }
  .title-container h2 {
    font-size: 4.5vw;
  }
}
@media (max-width: 400px) {
  .title-container {
    padding: 0 20px;
  }
}
</style>
