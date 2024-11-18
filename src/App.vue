<script setup>
import FooterMain from './components/FooterMain.vue'
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="flex items-center justify-between gap-4">
    <nav >
      <RouterLink to="/"><span class="font-bold text-xl text-[#00bd7e]">HeroLogo</span> </RouterLink>
      <div class="menu lg:flex hidden">
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="catalogue">Catalogue</RouterLink>
        <RouterLink to="blog">Blog</RouterLink>
        <RouterLink to="contact" id="contact">Contact</RouterLink>
      </div>
      <div class="contact">
        <p class="lg:flex hidden">00212 (617541079)</p>
        <RouterLink to="#">Call me back</RouterLink>
      </div>
    </nav>
  </header>

  <RouterView />
  <FooterMain />
</template>

<style scoped>
header {
  width: 100%;
  max-width: 1024px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1024px;
  width: 100% !important;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
  gap: 4rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

.contact {
  display: flex;
  gap: 3;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }


  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
