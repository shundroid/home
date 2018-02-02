<template lang="pug">
  main
    h2 Projects
    h5 More projects on #[a(href="https://github.com/shundroid?tab=repositories") Github].
    section
      Project(title="asterisks" background="#333" color="#cfe3cb" link="https://asterisks.netlify.com")
        img(slot="thumbnail" src="../assets/asterisks.png")
        | My blog for everything.
      Project(title="animium.js" background="#FF9800" color="#fff" link="https://github.com/dengaku-club/animium.js")
        img(slot="thumbnail" src="../assets/animium.png")
        | Developed with #[a(href="https://dengaku.club/") dengaku-club].
        br
        | We held #[a(href="https://dengaku.club/workshops/archives/20170826-cganimation/") a workshop]
        | &nbsp;explaining how animation works.
        br
        | We used this in the workshop.
      Project(:no-image="true" title="hexo-search-result" background="#0f83cd" color="#fff" link="https://github.com/shundroid/hexo-search-result")
        | You can make a search result page for #[a(href="https://github.com/PaicHyperionDev/hexo-generator-search") hexo-generator-search]
        | &nbsp;by using this.
      Project(:no-image="true" title="sphero-editor" background="#009688" color="#fff" link="https://github.com/comozilla/sphero-editor")
        | Developed with #[a(href="http://comozilla.org/") Comozilla Lab].
        br
        | We held a workshop about #[a(href="https://www.sphero.com/") sphero] bowl.
        br
        | This was used in the workshop to program sphero by javascript.
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
  font-family: 'Electrolize', arial;
}
h2 {
  font-size: 2em;
  margin: 50px 0 20px 0;
}
h5 {
  font-weight: normal;
  margin-bottom: 50px;
}
section {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
