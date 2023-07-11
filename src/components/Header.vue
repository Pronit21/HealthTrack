<template>
    <v-app>
      <v-app-bar app color="white" light elevation="6" elevate-on-scroll>
        <v-toolbar-title class="text-h5 font-weight-bold" color="purple">
          <img src="./../assets/HealthTraq.jpg" alt="">
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-list class="d-flex align-center" :class="menuClass">
          <v-list-item link v-for="(menu, index) in menus" :key="index" :to="menu.route">
            <v-list-item-title class="text-uppercase font-weight-bold" >{{ menu.title }}</v-list-item-title>
          </v-list-item>
          <v-btn icon class="mr-3" :class="searchClass">
            <v-icon size="24px">mdi mdi-magnify</v-icon>
          </v-btn>
          <v-btn class="mr-3" @click="navigateToLogin()" :class="loginClass">Login</v-btn>
        </v-list>
      </v-app-bar>
    </v-app>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        menus: [
          { title: 'Home', route: 'home' },
          { title: 'About us', route: 'about-us' },
          { title: 'Portfolio', route: 'portfolio' },
          { title: 'Fitness', route: 'fitness' },
          { title: 'Gallery', route: 'gallery' },
          { title: 'Contact', route: 'contact' },
        ],
        menuClass: '',
        searchClass: '',
        loginClass: '',
      };
    },
    mounted() {
      window.addEventListener('resize', this.onResize);
      this.onResize();
    },
    beforeDestroy() {
      window.removeEventListener('resize', this.onResize);
    },
    methods: {
      navigateToLogin() {
        window.location = "http://localhost:8081/";
      },
      
      
    },
  };
  </script>
  
  <style scoped>
  .v-toolbar-title {
    font-size: 32px;
    font-family: 'Montserrat', sans-serif;
    color: #4f4f4f;
    text-transform: uppercase;
  }
  
  .v-list-item-title {
    font-size: 14px;
    font-family: 'Montserrat', sans-serif;
    color: #4f4f4f;
    text-transform: uppercase;
  }
  
  .v-btn {
    font-size: 14px;
    font-family: 'Montserrat', sans-serif;
  }
  
  .v-btn--outlined {
    border-color: #4caf50;
    color: #4caf7c;
  }
  
  .v-btn--outlined:hover {
    border-color: #4caf50;
    background-color: #9bf19e;
    color: #fff;
  }
  
  .v-btn--outlined:focus {
    box-shadow: none;
  }
  
  .v-btn--icon:hover {
    background-color: transparent;
  }
  
</style>  