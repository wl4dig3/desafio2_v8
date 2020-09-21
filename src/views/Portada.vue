<template>
<div class="home">

    <h1>Bienvenidos al portal en construccion V8</h1>
</div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld.vue'

export default {
    name: 'Portada',
    components: {
        HelloWorld
    }
}
</script>

<style scoped>
.home {
    background: blueviolet;
    background-image: url("../assets/img/car_portada.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: 100%;
    display: flex;
    justify-content: center;
    /* align-items: center; */
    height: 50rem;
    color: black;
}
h1{
    margin-top:2rem ;
}
</style>