<template lang="pug">
article(:style="style")
  img(:src="thumbnail")
  h3
    a(:href="link" target="_blank" v-if="link") {{ title }}
    span(v-else) {{ title }}
  .slot-container
    slot
</template>

<script>
export default {
  props: {
    title: String,
    background: String,
    color: String,
    link: { type: String, required: false },
    thumbnail: { type: String, default: 'https://lh3.googleusercontent.com/D38C-EsaUIjY3T5u65KyXBAHVFty8oZT44v17uUBWezOGyUHxbeW0ZNhw32qrF7gZgu3tT1iaiWXghDFFzRjiohpA-QdYXKG1InPpxmjTIavzPRxUM-JWjpYgk3xo1h1aR8fORt92Fnm39Slg1JwgrSCTHtYCnytEVKUc6rvnDWNctpTxhl1nRz3QD4yhoHMV7auhMFQSZZED9uQ9H2mUMuXP6POzaaASlU3Q5g-9lWv1s2zyS_t37OxYEjvjTz-ex1_9BQWndHaTyHf54NaSrvjza0ZgTP6Zpg3AX9v8T6f5i9uwBAeOXIQPNOeV-2e49255ZGnSMfkF_9xnDBDCbCcYCeoySpX1nDDR8z0vu3fhiwfJfZOOYMR_BJwkffCfVgiPmeyHZbERM6HoL7mfcO4Qju2NFOyK8-y4RPDeHi0BK3w-bw91rrA3tJQFwGz0vlHaFLD_w4hqnpy-EJ8TwqzOWDni9aJbEE-zG_-womnQSwhQvrvJ_MIwz1mCWhASfQVyYBOPRpJR_Us9GQUq4kbSTjwm49vpeVvLVikEz64DdCTOOhTca-bqSgAJervtyCW_v9UoaV09sCpuw6O_03gtrh658Vysrvz_9JE3gvKuAirE2r7cGcYv2STxGcPil8L7zyDnHioa_ZpswDh3yNcWTlCATKGCeempVKK_fgeOOcfPyEJHJbQ49WXNx2lYAfv6EL1ctdA2UB8ikI6V-72=s256-no?authuser=0' }
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
  display: flex;
  flex-direction: column;
  align-items: center;
}
a {
  color: inherit;
}
img {
  width: 100px;
}
.slot-container {
  flex: 1;
  overflow-y: auto;
}
</style>

<style>
.slot-container a {
  color: inherit;
}
</style>
