<template>
<div class="navbarr" :class="{classA: scrollPosition < 50, classB: scrollPosition > 50}">

  <div class="container">
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <i class="fas fa-align-left"></i>
    </button>
      <a class="navbar-brand text-center" href="#"><div class="logo-sq">M</div></a>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li @click="$vuetify.goTo(first, easeOutQuart)" class="nav-item active">
          <a class="nav-link" href="#about">ABOUT ME</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#skills">SKILLS<span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#testimonials">TESTIMONIALS<span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#projects">PROJECTS</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#services">SERVICES</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#contact">CONTACT ME</a>
        </li>
      </ul>
      <ContactBtn />
    </div>
  </nav>
  </div>
</div>
</template>

<script>
import ContactBtn    from   '@/components/ContactBtn.vue'

export default {
  data () {
    return {
      scrollPosition : null
    }
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY
    }
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
  },
  components: {
    ContactBtn,
  }
}
</script>

<style scoped>
.navbarr {
  position: fixed;
  width: 100%;
  z-index: 1000
}
.classA .navbar-light .navbar-toggler {
    color: rgb(8, 8, 8);
    border: none
}
.classB .navbar-light .navbar-toggler {
    color: rgb(231, 231, 231);
    border: none
}

.classB {
    animation-name: bcChange;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
    border-bottom: #575656 solid 1px;
}
@keyframes bcChange {
  0%    {height:110px; background-color: rgba(33, 33, 33, 0)}
  100%  {height:55px; background-color: rgba(33, 33, 33, 1);}
}

.classB .container {
    animation-name: paddingChange;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes paddingChange {
  0%    {padding: 24px}
  100%  {padding: 0}
}
.classB .logo-sq {
    animation-name: logoChange;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes logoChange {
  0%    {width: 60px;height: 60px;color: black}
  100%  {width: 40px;height: 40px;color: #fcfcfc}
}
.classB .nav-link {
    animation-name: liChange;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes liChange {
  0%    {color: black}
  100%  {color: #fcfcfc}
}

.classA {
    animation-name: bcChangeBack;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes bcChangeBack {
  0%  {height:55px; background-color: rgba(33, 33, 33, 1);}
  100%    {height:110px; background-color: rgba(33, 33, 33, 0)}
}
.classA .container {
    animation-name: paddingChangeBack;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes paddingChangeBack {
  0%  {padding: 0}
  100%    {padding: 24px}
}
.classA .logo-sq {
    animation-name: logoChangeBack;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}
@keyframes logoChangeBack {
  0%  {width: 40px;height: 40px;color: #fcfcfc}
  100%    {width: 60px;height: 60px;color: black}
}
.classB a:hover {
    color: #fcfcfc !important;
    text-decoration: none !important;
}
.classB .btn-secondary {
    color: #fcfcfc;
    background-color: #212121;
    border-color: #212121;
    border-radius: 0;
    padding: 10px;
    font-weight: bold;
}

.bg-light {
    background-color: transparent !important;
}
.logo-sq {
    width: 60px;
    height: 60px;
    display: flex;
    align-content: center;
    align-items: center;
    justify-content: center;
    border: solid 2px;
    border-radius: 50%;
    font-size: 34px;
}
.nav-link {
    font-size: 14px;
}
</style>
