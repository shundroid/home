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
        | Developed with #[a(href="https://dengaku.club/") dengaku-club].#[br]
        | We held #[a(href="https://dengaku.club/workshops/archives/20170826-cganimation/") a workshop]
        | &nbsp;explaining how animation works.#[br]
        | We used this in the workshop.
      Project(:no-image="true" title="hexo-search-result" background="#0f83cd" color="#fff" link="https://github.com/shundroid/hexo-search-result")
        | You can make a search result page for #[a(href="https://github.com/PaicHyperionDev/hexo-generator-search") hexo-generator-search]
        | &nbsp;by using this.
      Project(:no-image="true" title="sphero-editor" background="#009688" color="#fff" link="https://github.com/comozilla/sphero-editor")
        | Developed with #[a(href="http://comozilla.org/") Comozilla Lab].#[br]
        | We held a workshop about #[a(href="https://www.sphero.com/") sphero] bowl.#[br]
        | This was used in the workshop to program sphero by javascript.
      Project(:no-image="true" title="hexo-embed-hatena-blog-card" background="#9C27B0" color="#fff" link="https://github.com/shundroid/hexo-embed-hatena-blog-card")
        | Use #[a(href="http://help.hatenablog.com/entry/blogcards") Hatena Blog Card] on hexo.
        | I'm using now on my blog.
      Project(:no-image="true" title="sphero-websocket" background="#F44336" color="#fff" link="https://github.com/shundroid/sphero-websocket/tree/develop")
        | Control sphero via web-socket.
        | We have used this in the workshops which develop sphero-apps.
      Project(:no-image="true" title="virtual-sphero" background="#3F51B5" color="#fff" link="https://github.com/comozilla/virtual-sphero/tree/develop")
        | We can simulate spheros when we don't have them.
        | It was very useful when we developed.
      Project(:no-image="true" title="themusic" background="#e0e0e0" color="#212121" link="https://github.com/chikoski/themusic")
        | A music player on Firefox OS.
        | Developed with #[a(href="https://github.com/chikoski") chikoski], a student who was during work visit.
      Project(:no-image="true" title="threejs-kart" background="#43A047" color="#FFD180" link="https://github.com/shundroid/threejs-kart")
        | Developed in the workshop about three.js.
        | This is what I used Git for the first time, so the commit message is very strange.
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
