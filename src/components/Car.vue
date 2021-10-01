<template>
  <h2>Coche</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Las potencias para transitar en zona urbana deben ser menor a 300CV</p>
    <ul>
        <template v-for= "(power, index) in powers" :key="index">
            <li v-if="power<200">
            {{power}}
            </li>
        </template>

    </ul>
    <p>Las potencias para transitar en carretera deben ser igual o mayor a 200CV</p>
    <ul>
        <template v-for= "(power, index) in powers" :key="index">
            <li v-if="power>=200">
            {{power}}
            </li>
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