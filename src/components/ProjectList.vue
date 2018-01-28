<template>
  <main>
    <h2>Projects</h2>
    <section>
      <Project title="asterisks" background="#333" color="#cfe3cb" link="https://asterisks.netlify.com">
        <img slot="thumbnail" src="../assets/asterisks.png" />
        My blog for everything.
      </Project>
    </section>
  </main>
</template>

<script>
import Project from './Project.vue'

export default {
  components: {
    Project
  }
}
</script>

<style scoped>
main {
  text-align: center;
}
section {
  display: flex;
  justify-content: center;
}
</style>
