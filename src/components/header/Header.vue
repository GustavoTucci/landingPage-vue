<template>
  <header class="header" :class="{ 'scrolled': hasScrolled }">
    <nav class="nav-container">
      <div class="logo-container">
        <h1 class="logo">
          <span class="logo-gradient">ARCHVIZ</span>
          <span class="logo-dot"></span>
        </h1>
      </div>

      <button class="mobile-menu-button" 
              @click="toggleMenu"
              :class="{ 'active': isMenuOpen }">
        <span></span>
        <span></span>
        <span></span>
      </button>

      <div class="nav-links" :class="{ 'active': isMenuOpen }">
        <a href="#home" class="nav-link" @click="closeMenu">Home</a>
        <a href="#portfolio" class="nav-link" @click="closeMenu">Portfólio</a>
        <a href="#servicos" class="nav-link" @click="closeMenu">Soluções</a>
        <a href="#contato" class="nav-link" @click="closeMenu">Contato</a>
        <a href="#contato" class="nav-cta" @click="closeMenu">Solicitar proposta</a>
      </div>
    </nav>
  </header>
</template>

<script>
import './Header.css'

export default {
  name: 'MainHeader',
  data() {
    return {
      isMenuOpen: false,
      hasScrolled: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
      document.body.style.overflow = this.isMenuOpen ? 'hidden' : ''
    },
    closeMenu() {
      this.isMenuOpen = false
      document.body.style.overflow = ''
    },
    handleScroll() {
      this.hasScrolled = window.scrollY > 20
    }
  }
}
</script>

<style>
</style> 