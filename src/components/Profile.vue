<template lang="pug">
main
  h2 Profile
  img(src="https://farm5.staticflickr.com/4667/39297562435_28c17bcf44_o_d.png")
  section
    .description
      .select-lang
        span(:class="{ 'active-lang': isJa }" @click="ja") Japanese
        | /
        span(:class="{ 'active-lang': !isJa }" @click="en") English
      h3 shundroid
      span(v-if="isJa") 2002年生まれ。今は大学生です。
      span(v-else) I was born in 2002. Now I'm a university student.
      h3(v-if="isJa") 趣味
      h3(v-else) My hobby
      span(v-if="isJa") プログラミング、数学、ピアノ、作問、耳コピ
      span(v-else) Programming, Math, Piano, Creating questions for exams and Copy down tunes by ear.
      h3(v-if="isJa") プログラミングについて
      h3(v-else) Programming
      span(v-if="isJa") プログラミングは10年目です。
      span(v-else) I have been programming for 10 years.
      h4(v-if="isJa") 専門でやっている言語
      h4(v-else) Languages I specialize in
      | JavaScript / TypeScript
      p(v-if="isJa")
        | 実用システムのチーム開発経験があります。コードレビューなども可能です。#[br]
        | 主に子どもに技術を広めるワークショップに使うシステムを作ってきました。#[br]
      p(v-else)
        | I have experienced collaborative Web development in practical situations. I can review codes. #[br]
        | Mainly I have developed systems for workshops which aim to spread technologies to children.
      h4(v-if="isJa") 使える言語
      h4(v-else) Languages I can use
      | (Often use) C# (both .NET and unity) / python#[br]
      | (Sometimes use) Rust, Swift, Ruby, Visual Basic, Lua
      h3(v-if="isJa") 受賞歴・検定など
      h3(v-else) Achievements, qualifications, etc
      p(v-if="isJa")
        | 2017＜検定＞P検2級取得#[br]
        | 2013-2016＜ロボティクスプログラミング＞FLL Japan Open 4年連続出場#[br]
        | 2015＜所属団体・システム開発担当＞ワークショップアワード 最優秀賞受賞#[br]
        | 2014＜コンテスト＞Mashup Awards 11 Open Web Apps 部門賞受賞#[br]
        | 2014＜コンテスト＞HTML Japan Cup 2014 Webプラットフォーム賞受賞#[br]
      p(v-else)
        | 2017＜Qualification＞ICT Proficiency Exam: Grade 2#[br]
        | 2013-2016＜Robotics Programming＞Participated in FLL Japan Open for four years#[br]
        | 2015＜Organization I have joined / I was in charge of system development＞Workshop Awards Grand Prize#[br]
        | 2014＜Contest＞Mashup Awards 11 Open Web Apps Prize#[br]
        | 2014＜Contest＞HTML Japan Cup 2014 Web Platform Prize
      | More about me: #[a(href="https://asterisks.netlify.app/profile/") See my blog]
</template>

<script>
export default {
  data() {
    return {
      isJa: true
    };
  },
  methods: {
    ja() {
      this.isJa = true;
    },
    en() {
      this.isJa = false;
    }
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
  margin: 50px 0;
}
h5 {
  margin: 0;
}
section {
  display: flex;
  justify-content: center;
}
.description {
  text-align: left;
  line-height: 2em;
}
.select-lang {
  text-align: center;
}
.select-lang span {
  text-decoration: underline;
}
span.active-lang {
  text-decoration: none;
}
</style>
