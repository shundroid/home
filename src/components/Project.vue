<template lang="pug">
article(:style="style")
  img(:src="thumbnail")
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
    thumbnail: { type: String, default: '/src/assets/no-image.png' }
  },
  computed: {
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
