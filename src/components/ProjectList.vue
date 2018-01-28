<template>
  <main>
    <h2>Projects</h2>
    <section>
      <Project title="asterisks" background="#333" color="#cfe3cb" link="https://asterisks.netlify.com">
        <img slot="thumbnail" src="../assets/asterisks.png" />
        My blog for everything.
      </Project>
      <Project title="animium.js" background="#FF9800" color="#fff" link="https://github.com/dengaku-club/animium.js">
        <img slot="thumbnail" src="../assets/animium.png" />
        Developed with <a href="https://dengaku.club/">dengaku-club</a>.<br />
        We held <a href="https://dengaku.club/workshops/archives/20170826-cganimation/">a workshop</a> explaining how animation works.<br />
        We used this in the workshop.
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
