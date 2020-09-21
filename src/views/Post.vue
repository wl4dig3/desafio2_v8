<template>
<div class="post">
    <h1 v-text="tituloEntrada">Titulo Entrada</h1>
    <h2>Post</h2>
    <router-link :to=" paginar(false)">Anterior</router-link>
    <router-link :to="paginar(true)">Siguiente</router-link>
    <br />
    <router-link :to="{name:'comentarios'}">Comentarios</router-link>
    <router-view></router-view>
</div>
</template>

<script>
export default {
    methods: {
        paginar(siguiente) {
            let entrada = parseInt(this.$route.params.entrada);

            if (siguiente)
                return entrada < 10 ? `/post/${entrada + 1}` : `/post/${entrada}`;
            else
                return entrada > 1 ? `/post/${entrada - 1}` : `/post/${entrada}`;
        },
    },
    computed: {
        tituloEntrada() {
            return `Entrada ${this.$route.params.entrada} del Blog`;
        },
    },
};
</script>

<style lang="scss" scoped>
.post {
  background: blueviolet;
  background-image: url("../assets/img/car_post.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: 100%;
  display: flex;
  flex-direction: column;
  height: 50rem;
  color: black;

  h1,
  h2 {
    margin-top: 1rem;
  }
  a {
      color: black;
      font-size: 1.3em;
  }
}
</style>