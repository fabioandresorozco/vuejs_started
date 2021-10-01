<template>
  <h2>Coche - Composition API</h2>
  <p>Marca: {{brand}}</p>
  <p>Modelo: {{model}}</p>


</template>

<script>
export default {
    setup(){
        const brand = "Renault";
        const model = "Megane";
      
        return {
            brand, model, 
        }
    }
}
</script>

<style>

</style>