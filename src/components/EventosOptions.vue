<template>
      <h1>Eventos con VueJs OPtions</h1>

      <h2>Coche - OPtion API</h2>
      <p>Marca: {{brand}}</p>
      <p>Modelo: {{model}}</p>
      <p>Potencia: {{power}}</p>

      <button @click="upPower(50)">Aumentar</button>
      <button @click="downPower()">Disminuir</button>

</template>
<script>
      export default{
            data(){
                  return {
                        brand: "Seat",
                        model:"Leon",
                        power: 50   
                  }
                  
            },
            methods:{ // Objeto que contendrá metodos que serán llamados desde un evento.
                  upPower(newPower) {
                        //alert("Aumentando potencia a " + newPower);
                        this.power += newPower;
                  },
                  downPower(){
                        alert("Disminuyendo potencia...");
                        this.power--;
                  }            
            }
      }
</script>
<style>
</style>