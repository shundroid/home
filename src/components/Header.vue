<template>
  <header>
    <section class="title-container">
      <h1>Shundroid</h1>
      <h2>
        A junior high school student,<br />
        A web programmer
      </h2>
    </section>
    <Motiv />
  </header>
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
  padding: 0 100px;
  box-sizing: border-box;
  height: calc(100% - 300px);
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
  margin-left: 20px;
  font-size: 3vh;
}
</style>
