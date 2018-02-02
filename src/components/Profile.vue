<template lang="pug">
  main
    h2 Profile
    section
      img(src="https://farm5.staticflickr.com/4685/24557689617_9b8ac248cc_m_d.jpg")
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
  margin-left: 10px;
  line-height: 2em;
}
.small {
  font-size: 0.1em;
}
</style>
