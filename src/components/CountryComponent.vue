<script>
export default {
  name: "CountryComponent",
  props: [
    "name",
    "capital",
    "currency_name",
    "currency",
    "region",
    "code",
    //TODO: crear una propiedad para determinar si al componente se le puede hacer click
  ],
};
</script>
<template>
  <!--TODO: Utilizar la propiedad creada para controlar el click. Cuando el componente es "clickeable", redirigir a la pagina del pais.
  Mira las rutas para ver como redirigir al usuario.-->
  <div class = "country"
    > 


  <!--TODO: Poblar el HTML con las propiedades. Usar https://countryflagsapi.com/png/${code}-->
  
  <img 
      :src= "`https://countryflagsapi.com/png/${code}`"
      width="200"
      height="200"
    />
    <h1 class = "nombre"
    > {{name}} </h1>
    <h1 class = "capital"> Capital: {{capital}} </h1>
    <h1 >  Moneda: {{currency_name}} ({{currency}}) </h1>
    <h1 > Región: {{region}} </h1>
  </div> 
</template>

<style scoped>
.country {
  padding: 2px;
  white-space: nowrap;
  width: 350px;
  height: 350px;
  border-style: solid;
  border-radius: 5px;
  border-color: grey;
  cursor: pointer;
}

.nombre{
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 2em;
}
.capital{
   overflow: hidden;
  text-overflow: ellipsis;
  font-size: 1.5em;
}
.country:hover {
  background-color: rgb(49, 49, 49);
  cursor: pointer;
}

h1 {
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 1.em;
}
</style>
