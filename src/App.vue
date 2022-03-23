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
          .my-3 在擔任代理教師的期間，覺得應該好好地為未來職涯作好規劃。
          .my-3 因自己在遊玩遊戲時，接觸了許多程式設計師寫出的MOD，因緣際會下，對程式設計產生了興趣。
          .my-3 隨後參與了前端網頁開發技術的專業課程，在半年的訓練中習得了 HTML、CSS、JavaScript 及 Vue.js 等技術，能使用 Node.js 與 MongoDB 建置後端資料庫，並部署於 heroku 完成前後端整合的專案。
          .my-3 在學習的過程中，亦經歷了許多挫折，不過每次的失敗都是成長的基石，而我也持續學習各種解決問題的方法。
          .my-3 前端開發的技術日新月異，需要透過不斷地學習以及經驗累積，我會繼續保持熱忱，迎接未來的每一個挑戰，成為與時俱進的前端工程師。
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
    .row
      .col-12
        .title RESUME
      .row.px-3.px-lg-0
        .col-12.mt-5
          .row
            .col-lg-6.my-3
              .resume-title Education
              .resume-board.px-3
                .resume-subtitle 勞動部勞動力發展署 泰山前端網頁開發技術班
                p 2021 / 09 ~ 2022 / 03
                ul 學習技術
                  li HTML/CSS/Bootstrap/SASS
                  li JavaScript/jQuery/Vue.js
                  li Node.js/Express.js/MongoDB/Git
              .resume-board.px-3
                .resume-subtitle 中華大學 應用日語學系
                p 2015 / 09 ~ 2019 / 06
                ul
                  li 主修應用日語學系，求學期間積極精進自己的語言能力，並在大二時期考取日文檢定 N2 證照。
            .col-lg-6.my-3
              .resume-title Work Experience
                .resume-board.px-3
                  .resume-subtitle 苗栗縣 三灣國民小學
                  p 2021 / 02 ~ 2021 / 07
                  ul
                    li 擔任數學及自然科任教師
              .resume-board.px-3
                .resume-subtitle 苗栗縣 照南國民小學
                p 2021 / 02 ~ 2021 / 07
                ul
                  li 擔任課後輔導教師
              .resume-title Language Skill
                .resume-board.px-3
                  ul.language-ul Chinese
                    li Native Language
                .resume-board.px-3
                  ul.language-ul Japanese
                    li JLPT N2
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
                  a.btn.px-2.py-1(href="https://ainoi.github.io/monoaka-front/" target="_blank") Go to Page
              .col-lg-5.my-5.mx-4
                .row
                  .col-12.px-2
                    .monoaka-title
                      .row
                        .col-12 Mono's Archive
                        .col-12 文作分享網站
                    .monoaka-text
                      .mt-2 為文章創作者製作的文作分享網站，可以刊登自己嘔心瀝血的創作，並自動推播至首頁最新位置。
                      .mt-2 成為用戶在閱讀後，可以選擇啟用「黑暗模式」，讓讀者方便閱讀。
                  .col-12.monoaka-tab-group.mt-5
                    .monoaka-tab SCSS
                    .monoaka-tab Axios
                    .monoaka-tab Vue.js
                    .monoaka-tab Node.js
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
      .col-lg-4.px-lg-2.mb-5.card-filter
        .card.others-card
          .others-sample
            img.card-img-top(src="./assets/pomodoro.png")
            .others-bg-filter
            a.btn.px-2.py-1(href="https://ainoi.github.io/pomodoro/" target="_blank") Go to Page
          .card-body.px-3.py-3
            .row
              .col-12
                .card-title 番茄鐘 Pomodoro
                .card-text.my-4 參考他人的設計稿，並且以 Vue cli 開發番茄鐘網站，使用了 Vuex 、 PWA 技術及 chart.js 套件。
              .col-12.others-card-tab-group
                .others-card-tab SCSS
                .others-card-tab pug
                .others-card-tab Vue.js
                .others-card-tab Node.js
      .col-lg-4.px-lg-2.mb-5.card-filter
        .card.others-card
          .others-sample
            img.card-img-top(src="./assets/Template-img.png")
            .others-bg-filter
            a.btn.px-2.py-1(href="https://ainoi.github.io/Template-model/foodside.html" target="_blank") Go to Page
          .card-body.px-3.py-3
            .row
              .col-12
                .card-title LAFETERIA
                .card-text.my-4 從 TemplateMonster 網站中挑選樣板，在不使用 UI 框架下(如: bootstrap 等框架)，刻出相同版面，此外也運用許多 JavaScript、jQuery製作。
              .col-12.others-card-tab-group
                .others-card-tab CSS
                .others-card-tab HTML
                .others-card-tab JavaScript
                .others-card-tab jQuery
      .col-lg-4.px-lg-2.mb-5.card-filter
        .card.others-card
          .others-sample
            img.card-img-top(src="./assets/kurareshi.png")
            .others-bg-filter
            a.btn.px-2.py-1(href="https://github.com/AINOI/FF14Kurareshi" target="_blank") Go to Page
          .card-body.px-3.py-3
            .row
              .col-12
                .card-title LineBot-FF14 クラレシ
                .card-text.my-4 在 Node.js 環境下，搭配 Linebot 套件、 FF14 Restanet 及 Eorzea Database ，製作的 Line 機器人。為 FF14 用戶查詢所需要的製作列表。
              .col-12.others-card-tab-group
                .others-card-tab Linebot
                .others-card-tab Axios
                .others-card-tab Node.js
                .others-card-tab Express.js
      .col-lg-4.px-lg-2.mb-5.card-filter
        .card.others-card
          .others-sample
            img.card-img-top(src="./assets/ClayPigeon.png")
            .others-bg-filter
            a.btn.px-2.py-1(href="https://ainoi.github.io/clayPigeon-AINOI/Clay%20Pigeon.html" target="_blank") Go to Page
          .card-body.px-3.py-3
            .row
              .col-12
                .card-title 飛靶射擊 Clay Pigeon
                .card-text.my-4 使用 jQuery 打造的小遊戲。在一分鐘內利用滑鼠擊碎飛靶，遊戲當中要避免擊落鴿子，每擊碎一個飛靶就得一分，擊落一隻鴿子減一分。
              .col-12.others-card-tab-group
                .others-card-tab HTML
                .others-card-tab CSS
                .others-card-tab jQuery
      .col-lg-4.px-lg-2.mb-5.card-filter
        .card.others-card
          .others-sample
            img.card-img-top(src="./assets/majong.png")
            .others-bg-filter
            a.btn.px-2.py-1(href="https://ainoi.github.io/majong-AINOI/index(openThisFirst).html" target="_blank") Go to Page
          .card-body.px-3.py-3
            .row
              .col-12
                .card-title 麻將對對和
                .card-text.my-4 使用 jQuery 打造的小遊戲。翻開畫面上的牌，選擇加入手牌與否，並湊成對對和牌行型。
              .col-12.others-card-tab-group
                .others-card-tab HTML
                .others-card-tab CSS
                .others-card-tab jQuery
      .col-lg-4.px-lg-2.mb-5.card-filter
        .card.others-card
          .others-sample
            img.card-img-top(src="./assets/kingyosukui.png")
            .others-bg-filter
            a.btn.px-2.py-1(href="https://ainoi.github.io/kigyosukui-AINOI/kingyo.html" target="_blank") Go to Page
          .card-body.px-3.py-3
            .row
              .col-12
                .card-title 撈金魚 金魚すくい
                .card-text.my-4 使用 JavaScript 製作的撈金魚遊戲，在 20 秒內點擊畫面出現的金魚，每撈到一隻得一分，最後會顯示最高分及最高分者。
              .col-12.others-card-tab-group
                .others-card-tab HTML
                .others-card-tab CSS
                .others-card-tab JavaScript
section#contact
  .container-fluid.position.my-5
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
          a.profile-btn.mx-3(href="https://www.facebook.com/profile.php?id=100004781504538" target="_blank")
            i.bi.bi-facebook
          a.profile-btn.mx-3(href="mailto: aino30274@gmail.com")
            i.bi.bi-envelope-fill
      .col-1.col-sm-2
footer#footer
  .container-fluid
    .text-center.footer-copyright Copyright © 2022 Aino Studio. All rights reserved.
</template>
