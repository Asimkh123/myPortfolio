<template>
    <div id="navbar">
      <div class="container">
        <div id="logo"></div>
        <nav :class="{ 'open': menuOpen }">
          <button class="menu-button" @click="toggleMenu">☰</button>
          <div class="menu-items">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
            <router-link to="/projects">Projects</router-link>
            <router-link to="/contact">Contact</router-link>
          </div>
        </nav>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'NavBar',
    data() {
      return {
        menuOpen: false,
      };
    },
    methods: {
      toggleMenu() {
        this.menuOpen = !this.menuOpen;
      },
    },
  };
  </script>
  