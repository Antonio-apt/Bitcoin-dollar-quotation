<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Bitcoin Quotation</router-link> |
      <router-link to="/quotation">Dollar Quotation</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
  


  body{
    background-color:#293530;
    }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;

  }

  #nav {
    margin-left: 10px;
    margin-top: 15px; 
    a {
      font-weight: bold;
      text-decoration: none;
      color: #52685f;

      &.router-link-exact-active {
        color:#141a16 ;
      }
    }
  }
</style>