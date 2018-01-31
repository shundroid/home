<template lang="pug">
  article(:style="style")
    img(src="../assets/no-image.png" v-if="noImage")
    slot(name="thumbnail" v-else)
    h3
      a(:href="link" target="_blank") {{ title }}
    slot
</template>

<script>
export default {
  props: {
    title: String,
    background: String,
    color: String,
    link: String,
    noImage: { type: Boolean, default: false }
  },
  computed: {
    src() {
      return `./assets/${this.slug}.png`
    },
    style() {
      return {
        color: this.color,
        backgroundColor: this.background
      }
    }
  }
}
</script>

<style scoped>
article {
  width: 300px;
  height: 400px;
  padding: 30px;
  box-sizing: border-box;
  margin: 5px;
}
a {
  color: inherit;
}
h3 a {
  text-decoration: none;
}
img {
  width: 100px;
}
</style>
