<template lang="pug">
  main
    h2 Profile
    section
      img(src="https://farm5.staticflickr.com/4667/39297562435_28c17bcf44_o_d.png")
      .description
        | I was born on 15th October 2002. #[br]
        | I’m a junior high school student in Tokyo.#[br]
        | I love computer / robotics programming, #[br]
        | so I’ve joined various events to learn technologies since I was ten.#[br]
        | Recently, to help Web technologies spread#[br]
        | I held the workshops for elementary school students and developed applications.#[br]
        .small In fact, I have perfect pitch but I cannot read musical scores.
</template>

<style scoped>
main {
  text-align: center;
  font-family: 'Electrolize', arial;
}
h2 {
  font-size: 2em;
  margin: 50px 0;
}
section {
  display: flex;
  justify-content: center;
}
.description {
  text-align: left;
  margin-left: 50px;
  line-height: 2em;
}
img {
  margin-left: 100px;
}
.small {
  font-size: 0.1em;
}
</style>
