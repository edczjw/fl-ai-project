<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <RouterLink to="/" class="logo"
      ><img alt="Vue logo" src="@/assets/images/logo.png"
    /></RouterLink>
    <div class="wrapper">
      <nav>
        <!-- <RouterLink to="/">产品介绍</RouterLink>
        <RouterLink to="/about">关于我们</RouterLink> -->
        <RouterLink to="/contact" class="btn-use btn-3"><span>开始试用</span></RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped lang="scss">
header {
  width: 100%;
  height: 70px;
  padding: 0 32px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  backdrop-filter: blur(8px);
  box-shadow: 0 2px 10px #0000000a;
  background: transparent;
  position: fixed;
  left: 0;
  top: 0;
  z-index: 9;
}

.logo {
  display: block;
  font-size: 0;
  width: 180px;
  height: 70px;
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
  width: 130px;
  height: 40px;
  line-height: 40px;
  color: #fff;
  border-radius: 5px;
  text-align: center;
  font-family: 'Lato', sans-serif;
  font-weight: 500;
  background: transparent;
  cursor: pointer;
  transition: all 0.3s ease;
  position: relative;
  display: inline-block;
  box-shadow: inset 2px 2px 2px 0px rgba(255, 255, 255, 0.5), 7px 7px 20px 0px rgba(0, 0, 0, 0.1),
    4px 4px 5px 0px rgba(0, 0, 0, 0.1);
}

/* 3 */
.btn-3 {
  background: #00faca;
  background: linear-gradient(0deg, #11b896 0%, #00faca 100%);
  width: 130px;
  height: 40px;
  line-height: 42px;
  padding: 0;
  color: #fff;
  border: none;
}
.btn-3 span {
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
}
.btn-3:before,
.btn-3:after {
  position: absolute;
  content: '';
  right: 0;
  top: 0;
  background: #fff;
  transition: all 0.3s ease;
}
.btn-3:before {
  height: 0%;
  width: 2px;
}
.btn-3:after {
  width: 0%;
  height: 2px;
}
.btn-3:hover {
  background: transparent;
  box-shadow: none;
}
.btn-3:hover:before {
  height: 100%;
}
.btn-3:hover:after {
  width: 100%;
}
.btn-3 span:hover {
  color: #fff;
  font-weight: 600;
}
.btn-3 span:before,
.btn-3 span:after {
  position: absolute;
  content: '';
  left: 0;
  bottom: 0;
  background: #fff;
  transition: all 0.3s ease;
}
.btn-3 span:before {
  width: 2px;
  height: 0%;
}
.btn-3 span:after {
  width: 0%;
  height: 2px;
}
.btn-3 span:hover:before {
  height: 100%;
}
.btn-3 span:hover:after {
  width: 100%;
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
