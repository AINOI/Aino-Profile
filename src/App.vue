<script setup>
import { ref } from 'vue'
const scroll = ref(false)
window.addEventListener('scroll', () => {
  scroll.value = (window.scrollY > 0)
})

const navScroll = ref(false)
window.addEventListener('scroll', () => {
  navScroll.value = (window.scrollY > 0)
})

</script>

<template lang="pug">
#navbar.navbar.navbar-expand-lg.fixed-top.navbar-dark(:class="{ navScroll }")
  .container-fluid.px-5.my-2
    .logoBorder
      a.navbar-brand.logoBorderInner(href="#") HOME
    button.navbar-toggler.btn-white(type='button' data-bs-toggle='collapse' data-bs-target='#ainoLink')
      span.navbar-toggler-icon
    #ainoLink.collapse.navbar-collapse.justify-content-end
      ul.navbar-nav.mb-2.mb-lg-0
        li.nav-item.ms-5
          a.nav-link.linkHover(href="#about") ABOUT
        li.nav-item.ms-5
          a.nav-link.linkHover(href="#abilities") ABILITES
        li.nav-item.ms-5
          a.nav-link.linkHover(href="#resume") RESUME
        li.nav-item.ms-5
          a.nav-link.linkHover(href="#portfolio") PROTFOLIO
        li.nav-item.ms-5
          a.nav-link.linkHover(href="#contact") CONTACT
section#home(:class="{ scroll }")
  .titleBox
    .titleText
      p.text-center(v-if='!scroll') Aino Studio
      p.text-center(v-if='scroll') Web Designer
  .minebg
  .circleGroup
    .circle
    .circle
    .circle
    .circle
    .circle
    .circle
section#about
  .container.mb-5
    .row
      .col-12
        .title ABOUT ME
      .col-12.col-md-6.my-5
        .img-box
          img(src="./assets/self.jpg")
      .col-12.col-md-6.my-0.my-md-5.px-3
        .col-12
          .profile-title.my-3 許尚彬 SHANG BIN, HSU
          .my-3 Lorem ipsum dolor, sit amet consectetur adipisicing elit. Neque asperiores animi, id eligendi mollitia repellat velit expedita consequatur sint soluta, beatae fuga culpa totam nemo nam, sunt facilis tempore maiores.
          .my-3 Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta ipsum fugiat similique quidem blanditiis, mollitia quibusdam cupiditate velit debitis iure, vel veritatis suscipit esse a dignissimos dolores laborum beatae modi.
          .my-3 Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta ipsum fugiat similique quidem blanditiis, mollitia quibusdam cupiditate velit debitis iure, vel veritatis suscipit esse a dignissimos dolores laborum beatae modi.
        .col-12.d-flex
          a.profile-btn.mx-3(href="https://github.com/AINOI" target="_blank")
            i.bi.bi-github
          a.profile-btn.mx-3(href="mailto: aino30274@gmail.com")
            i.bi.bi-envelope-fill
section#abilities
  .container.mb-5
    .row
      .col-12
        .title ABILITIES
    .row.mt-5
      .col-12.col-md-4.my-2.my-md-0
        .card
          .card-body.ability-card.mt-2.mb-5
            .card-title.mb-4 DESIGN
            .card-icon
              i.bi.bi-palette-fill
            .card-text.mt-4
              p Photoshop
              p Illustrator
      .col-12.col-md-4.my-2.my-md-0
        .card
          .card-body.ability-card.mt-2.mb-5
            .card-title.mb-4 FRONTEND
            .card-icon
              i.bi.bi-file-earmark-code-fill
            ul.card-text.mt-4
              li HTML/CSS/SCSS
              li Bootstrap/Tailwind
              li JavaScript(ES6)/jQuery
              li Vue.js
      .col-12.col-md-4.my-2.my-md-0
        .card
          .card-body.ability-card.mt-2.mb-5
            .card-title.mb-4 BACKEND
            .card-icon
              i.bi.bi-server
            ul.card-text.mt-4
              li Node.js
              li npm
              li Express.js
              li MongoDB
section#resume
  .container.mb-5
    .row.h-100
      .col-12
        .title RESUME
section#portfolio
  .container
    .row
      .col-12
        .title PORTFOLIO
    .row.px-3
      .col-12.mx-auto.my-5.card-filter
        .card
          .card-body
            .row.d-flex.justify-content-center
              .col-lg-5.my-5.mx-4.px-2
                .monoaka-sample
                  img(src="./assets/Monoaka-img.png")
                  .monoaka-bg-filter
                    a.btn.px-2.py-1(href="#") Go to Page
              .col-lg-5.my-5.mx-4
                .row
                  .col-12.px-2
                    .monoaka-title Mono's Archive
                    .monoaka-text Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora quod recusandae itaque voluptatem assumenda alias exercitationem natus corporis perferendis pariatur dolore totam cumque quibusdam beatae enim quae, voluptas nihil voluptatum!
                  .col-12.monoaka-tab.mt-5
                    .monoaka-tab-item scss
                    .monoaka-tab-item Axios
                    .monoaka-tab-item Vue.js
                    .monoaka-tab-item Node.js
              .col-lg-5.my-5.mx-4.px-2
                ul 前端
                  li Vue 前端框架搭配 Bootstrap-Vue UI框架
                  li Vuex 管理前端狀態
                  li Axios 向後端伺服器請求資料
                  li 註冊與登入功能
                  li 文章發布、管理及瀏覽功能
              .col-lg-5.my-5.mx-4.px-2
                ul 後端
                  li Node.js 搭配 Express.js 建立伺服器
                  li MongoDB 作為後端資料庫，會員管理、文章管理、回報管理等等。
    .row.px-3
      .col-lg-4.px-lg-2.mb-5
        .card
          img.card-img-top(src="./assets/room.png")
          .card-body
            .card-title 番茄鐘 Pomodoro
            .card-text 參考他人的設計稿，並且以Vue cli開發番茄鐘網站，使用了Vuex、PWA技術及chart.js套件。
      .col-lg-4.px-lg-2.mb-5
        .card
          img.card-img-top(src="./assets/room.png")
          .card-body
            .card-title 番茄鐘 Pomodoro
            .card-text 參考他人的設計稿，並且以Vue cli開發番茄鐘網站，使用了Vuex、PWA技術及chart.js套件。
      .col-lg-4.px-lg-2.mb-5
        .card
          img.card-img-top(src="./assets/room.png")
          .card-body
            .card-title 番茄鐘 Pomodoro
            .card-text 參考他人的設計稿，並且以Vue cli開發番茄鐘網站，使用了Vuex、PWA技術及chart.js套件。
      .col-lg-4.px-lg-2.mb-5
        .card
          img.card-img-top(src="./assets/room.png")
          .card-body
            .card-title 番茄鐘 Pomodoro
            .card-text 參考他人的設計稿，並且以Vue cli開發番茄鐘網站，使用了Vuex、PWA技術及chart.js套件。
      .col-lg-4.px-lg-2.mb-5
        .card
          img.card-img-top(src="./assets/room.png")
          .card-body
            .card-title 番茄鐘 Pomodoro
            .card-text 參考他人的設計稿，並且以Vue cli開發番茄鐘網站，使用了Vuex、PWA技術及chart.js套件。
      .col-lg-4.px-lg-2.mb-5
        .card
          img.card-img-top(src="./assets/room.png")
          .card-body
            .card-title 番茄鐘 Pomodoro
            .card-text 參考他人的設計稿，並且以Vue cli開發番茄鐘網站，使用了Vuex、PWA技術及chart.js套件。
section#contact
  .container-fluid.h-100.position
    .row.w-100
      .col-1.col-sm-2
      .col-10.col-sm-8.board.py-3.px-2
        .col-12.mt-2
          .contact-title CONTACT
        .col-12.mt-5
          .contact-text
            p 感謝您撥冗時間瀏覽此履歷
            p 歡迎於以下方式與我聯繫
        .col-12.mt-5.d-flex.justify-content-center
          a.profile-btn.mx-3(href="https://github.com/AINOI" target="_blank")
            i.bi.bi-github
          a.profile-btn.mx-3(href="https://www.facebook.com" target="_blank")
            i.bi.bi-facebook
          a.profile-btn.mx-3(href="mailto: aino30274@gmail.com")
            i.bi.bi-envelope-fill
      .col-1.col-sm-2
footer#footer
  .container-fluid
    .text-center.footer-copyright Copyright © 2022 Aino Studio. All rights reserved.
</template>
