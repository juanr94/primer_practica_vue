<template>
  <Car></Car>
  <h1>Nuestro primer component Vue JS</h1>
  <EventosOptions/>
  <hr/>
  <EventosCompoitionApi :power="power" :correo="correo" :upPower="upPower"/>
</template>

<script>
  import Car from './components/Car.vue'
  import EventosOptions from './components/EventosOptions.vue'
  import EventosCompoitionApi from './components/EventosCompoitionApi.vue'

  
  export default{
    components:{
      Car,
      EventosOptions,
      EventosCompoitionApi
    },
    setup(){
      let power = 50;
      let correo = 'audi@gmail.com'
      const upPower = () => {
        console.log("Aumentar power...");
        power++;
      }

      return {
        power,
        correo,
        upPower,
      }
    }
  }
</script>

<style>

</style>