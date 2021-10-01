<template>
  <h2>Coche</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Potencias:</p>
    <ul>
        <template v-for= "(power, index) in powers" :key="index">
            <li v-if="power<100">Zona Rural: {{power}}</li>
            <li v-else-if="power===100">Zona Urbana: {{power}}</li>
            <li v-else>Zona de carretera: {{power}}</li>
        </template>

    </ul>
    


</template>

<script>
export default {
    setup(){
        const brand = "Renault";
        const model = "Megane";
        
        const powers = [40, 80, 120, 160, 200, 240, 280, 320];
        
        return {
            brand, model, powers
        }
    }
}
</script>

<style>

</style>