<template>
    <h1>Hola soy h1 de Car</h1>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laboriosam ullam quia atque corporis recusandae doloremque tempora! Autem illo adipisci fugiat pariatur, voluptatum libero eaque sint quam harum soluta officiis ipsam?</p>
    <h2>Marca: {{brand}}</h2>
    <h2>Modelo: {{model}}</h2>
    <h2>Color:
        <span v-for="(color, index) in colors" :key="index">
            {{index + 1}}:{{color}} &backsim;
        </span>
    </h2>

    <template v-for="power in powers">
        <li v-if="power < 280">Urbana: {{power}}</li>
        <li v-else-if="power === 280">Hibrido: {{power}}</li>
        <li v-else>Carrera: {{power}}</li>
    </template>

    <h2>Precio: {{price}}</h2>
    <h2>Poder: {{power}}</h2>.
    
    <h2>Mensaje: {{mensaje.text}}</h2>
</template>
<script>
    export default {
        /**
        * Creando variables en vue con api option.
        
        data() {
            return {
                brand: "Audi",
                model: "A4",
                color: ["Azúl", "Verde", "Rojo"],
                price:"38000",
                power:"180",
                mensaje: {
                    title: "Hola mundo"
                    , text:"Adios"
                }
            }
        }*/

        /**
         * Creando variables en vue con Composition API.
         */
        setup() {
           const brand = "Audi"; 
           const model = "A4";
           const colors = ["Azúl", "Verde", "Rojo"];
           const price = "38000";
           const power = "180";
           const mensaje = {title: "Hola mundo" , text:"Adios"};
           const powers  = [60, 80, 120, 160, 200, 280, 300, 390, 540, 600]

           return {
            brand,
            model,
            colors,
            price,
            power,
            mensaje,
            powers
           }
        }

    }
</script>
<style>
</style>