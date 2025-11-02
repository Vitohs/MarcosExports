<template>
  <header class="header">
    <img class="logo" src="../assets/mExports.svg" />
      <button class="menu-toggle" @click="toggleMenu" aria-label="Abrir menu" v-show="isMobile">
        <span :class="{'open': menuOpen}"></span>
        <span :class="{'open': menuOpen}"></span>
        <span :class="{'open': menuOpen}"></span>
      </button>
      <nav :class="{'open': menuOpen || !isMobile}">
        <ul>
          <li><a href="/">Início</a></li>
          <li><a href="/sobre-nos">Sobre Nós</a></li>
          <li><a href="/produtos">Produtos</a></li>
        </ul>
      </nav>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const menuOpen = ref(false);
const isMobile = ref(false);

function toggleMenu() {
  menuOpen.value = !menuOpen.value;
}

function checkMobile() {
  isMobile.value = window.innerWidth <= 768;
  if (!isMobile.value) menuOpen.value = false;
}

onMounted(() => {
  checkMobile();
  window.addEventListener('resize', checkMobile);
});
onUnmounted(() => {
  window.removeEventListener('resize', checkMobile);
});

</script>

<style scoped>
  .header {
    background-color: #003566;
    width: 100%;
    padding-left: 20px;
    min-height: 100px;
    display: flex;
    align-items: center;
    gap: 20px;
    position: relative;
  }
  .logo {
    height: 70px;
    width: auto;
    padding-left: 20px;
    object-fit: contain;
  }
  nav ul {
    display: flex;
    gap: 30px;
    list-style: none;
  }
  nav ul li {
    position: relative;
    cursor: pointer;
    font-size: 22px;
  }
  nav ul li::after {
    content: "";
    position: absolute;
    left: 50%;
    bottom: -4px;
    width: 0;
    height: 4px;
    background: white;
    transition: width 0.5s cubic-bezier(0.4, 0, 0.2, 1);
    border-radius: 2px;
    transform: translateX(-50%);
  }
  nav ul li:hover::after {
    width: 100%;
  }
  a {
    text-decoration: none;
    color: white;
  }
  .menu-toggle {
    display: none;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    background: none;
    border: none;
    cursor: pointer;
    z-index: 20;
    margin-left: auto;
  }
  .menu-toggle span {
    display: block;
    width: 28px;
    height: 4px;
    margin: 4px 0;
    background: #fff;
    border-radius: 2px;
    transition: 0.4s;
  }
  .menu-toggle span.open:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
  }
  .menu-toggle span.open:nth-child(2) {
    opacity: 0;
  }
  .menu-toggle span.open:nth-child(3) {
    transform: rotate(-45deg) translate(6px, -6px);
  }

@media (max-width: 768px) {
  .header {
    padding-left: 0;
    min-width: 100vw;
    width: 100vw;
    box-sizing: border-box;
    position: relative;
    justify-content: space-between;
  }
  .logo {
    padding-left: 10px;
    width: 230px;
  }
  .menu-toggle {
    display: flex;
    margin-right: 10px;
  }
  nav {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    width: 100vw;
    background: #003566;
    transition: max-height 0.3s ease;
    overflow: hidden;
    max-height: 0;
    z-index: 10;
    box-sizing: border-box;
  }
  nav.open {
    max-height: 500px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.2);
  }
  nav ul {
    flex-direction: column;
    gap: 0;
    padding: 0;
  }
  nav ul li {
    padding: 18px 0;
    text-align: center;
    font-size: 20px;
    border-bottom: 1px solid #fff2;
  }
  body, html {
    overflow-x: hidden;
  }
}
</style>
