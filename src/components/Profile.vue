<template lang="pug">
main
  h2 Profile
  img(src="https://farm5.staticflickr.com/4667/39297562435_28c17bcf44_o_d.png")
  section
    .description
      h3 shundroid
      | 2002年生まれ。今は大学生です。#[br]
      | I was born in 2002. Now I'm a university student.
      h3 趣味 / My hobby
      | プログラミング、数学、ピアノ、作問、耳コピ#[br]
      | Programming, Math, Piano, Creating questions for exams and Copy down tunes by ear.
      h3 プログラミングについて / Programming
      | プログラミングは10年目です。 I have been programming for 10 years.
      h4 専門でやっている言語 / Languages I specialize in
      | JavaScript / TypeScript #[br]
      | 実用システムのチーム開発経験があります。コードレビューなども可能です。#[br]
      | 主に子どもに技術を広めるワークショップに使うシステムを作ってきました。#[br]
      | I have experienced collaborative Web development in practical situations. I can review codes. #[br]
      | Mainly I have developed systems for workshops which aim to spread technologies to children.
      h4 使える言語 / Languages I can use
      | (Often use) C# (both .NET and unity) / python#[br]
      | (Sometimes use) Rust, Swift, Ruby, Visual Basic, Lua
      h4 受賞歴・検定など / Achievements, qualifications, etc
      | 2017＜検定＞P検2級取得#[br]
      | 2013-2016＜ロボティクスプログラミング＞FLL Japan Open 4年連続出場#[br]
      | 2015＜所属団体・システム開発担当＞ワークショップアワード 最優秀賞受賞#[br]
      | 2014＜コンテスト＞Mashup Awards 11 Open Web Apps 部門賞受賞#[br]
      | 2014＜コンテスト＞HTML Japan Cup 2014 Webプラットフォーム賞受賞#[br]
      | #[br]
      | 2017＜Qualification＞ICT Proficiency Exam: Grade 2#[br]
      | 2013-2016＜Robotics Programming＞Participated in FLL Japan Open for four years#[br]
      | 2015＜Organization I have joined / I was in charge of system development＞Workshop Awards Grand Prize#[br]
      | 2014＜Contest＞Mashup Awards 11 Open Web Apps Prize#[br]
      | 2014＜Contest＞HTML Japan Cup 2014 Web Platform Prize
      | #[br]
      | More about me: #[a(href="https://asterisks.netlify.app/profile/") See my blog]
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
h5 {
  margin: 0;
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
</style>
