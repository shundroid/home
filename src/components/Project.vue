<template>
  <article :style="style">
    <slot name="thumbnail" />
    <h3><a :href="link" target="_blank">{{ title }}</a></h3>
    <slot />
  </article>
</template>

<script>
export default {
  props: {
    title: String,
    background: String,
    color: String,
    link: String
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
}
a {
  color: inherit;
  text-decoration: none;
}
img {
  width: 100px;
}
</style>
