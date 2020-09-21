<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Portada</router-link>
      <router-link :to="{name:'contacto'}">Contacto</router-link>
      <router-link to="/sobremi/1">Sobre mi</router-link>
      <router-link to="/post">Ultimo Post</router-link>
    </div>
    <router-view />
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent';

export default {
    name:'app',
    components:{FooterComponent}
}
</script>

<style lang="scss" scoped>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  display: flex;
  flex-direction: row;
  justify-content: right;
  background: gray;

  a {
    font-weight: bold;
    color: whitesmoke;
    margin-left: 0.5rem;

    &.router-link-exact-active {
      color: lightgreen;
    }
  }
}
@import './assets/css/style.css' 
</style>
