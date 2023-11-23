<template>

    <h1>Composition API</h1>
    <h1>Primer H1 de prueba</h1>
    <h2>Coche - OPtion API</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Potencia:{{power}} </p>
    <p>Correo:{{correo}} </p>
    <button  @click="testPower()">Power UP</button>
</template>
<script>
    // Realiza una referencia a una variable 
    import {ref} from "vue"
    export default{
        props:{
            power:{
                type : Number,
                default : 60,
            }, correo:{
                type : String,
            },
            upPower : Function,
        },
        setup(props) {
            const brand = "Audi";
            const model = "A4";   
            let power = ref(36)            
          
            console.log(props);

            const testPower = () => {
                props.upPower();  
                power.value++;      
            }

            return {
                brand,
                model,
                testPower,
                power,
            }

        }    
    };
</script>
<style>
</style>