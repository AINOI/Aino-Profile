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

const test = document.getElementById('about')

const lastCircle = document.getElementsByClassName('circle:nth-child(6)')

</script>

<template lang="pug">
#navbar.navbar.navbar-expand-lg.fixed-top.navbar-dark(:class="{navScroll}")
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
            a.nav-link.linkHover(href="#resume") RESUME
          li.nav-item.ms-5
            a.nav-link.linkHover(href="#abilities") ABILITES
          li.nav-item.ms-5
            a.nav-link.linkHover(href="#portfolio") PROTFOLIO
          li.nav-item.ms-5
            a.nav-link.linkHover(href="#contact") CONTACT
section#home(:class="{scroll}")
  .titleBox
    .titleText
      p.text-center(v-if='!this.scroll') Aino Studio
      p.text-center(v-if='this.scroll') Web Designer
  .minebg
  .circleGroup
    .circle
    .circle
    .circle
    .circle
    .circle
    .circle
section#about
  .container.mb-5.mb-md-0
    .row
      .col-12
        .title ABOUT ME
      .col-12.col-md-6.my-5
        .img-box
          img(src="./assets/self.jpg")
      .col-12.col-md-6.my-0.my-md-5.ps-5
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
section#resume
  .container
    .row.h-100
      .col-12
        .title RESUME
section#abilities
  .container
    .row.h-100
      .col-12
        .title ABILITIES
section#portfolio
  .container
    .row.h-100
      .col-12
        .title PORTFOLIO
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

<style>

</style>