<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <RouterLink to="/" class="logo"><img alt="Vue logo" src="@/assets/logo.svg" /></RouterLink>
    <div class="wrapper">
      <nav>
        <!-- <RouterLink to="/">产品介绍</RouterLink>
        <RouterLink to="/about">关于我们</RouterLink> -->
        <RouterLink to="/contact" class="btn-use">开始试用</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped lang="scss">
header {
  width: 100%;
  height: 60px;
  padding: 0 32px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  backdrop-filter: blur(8px);
  background: transparent;
  box-shadow: 0 2px 10px #0000000a;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
}

.logo {
  display: block;
  font-size: 0;
  width: 220px;
  height: 50px;
  border: 1px solid #000;
  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
}

header .wrapper {
  height: 100%;
}
nav {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  font-size: 12px;
}

nav a.router-link-exact-active {
  color: #fff;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
nav .btn-use {
  color: #fff;
  height: 36px;
  line-height: 36px;
  font-size: 14px;
  font-weight: 500;
  background-color: #30c1c1;
  border-radius: 36px;
  box-shadow: 0 2px 10px #0000000a;
  &:hover{ 
    transform: scale(1.1);
  }
}
@media (min-width: 1024px) {
  .logo {
    margin: 0 2rem 0 0;
  }
  nav {
    font-size: 1rem;
  }
}
</style>
