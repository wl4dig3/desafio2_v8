<template>
  <div id="app">
    <div id="nav">
      <router-link :to="{name:'Portada'}">Portada</router-link>
      <router-link to="/contacto">Contacto</router-link>
      <router-link to="/sobremi">Sobre mi</router-link>
      <router-link to="/post/1">Ultimo Post</router-link>
    </div>
    <transition name="disappear" mode="out-in">
    <router-view />
    </transition>
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

.disappear-enter-active {
    transition: all 1s ease;
}
.disappear-leave-active {
    transition: all 2s cubic-bezier(1, 0.5, 0.9,1);
}
.disappear-enter,
.disappear-leave-to

{
    transform: translateX(20px);
    opacity: 0;
}

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
    color: black;
    margin-left: 0.5rem;

    &.router-link-exact-active {
      color: lightgreen;
    }
  }
}
@import './assets/css/style.css' 
</style>
