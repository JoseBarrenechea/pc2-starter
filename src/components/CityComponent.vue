<script>
export default {
  name: "CityComponent",
  props: [
    "name",
    "country_name",
    "country_code",
    "state_name",
    "state_code",
    "latitude",
    "longitude",
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
  
  
    <h1 class="nombre">{{ name }}</h1>
    <h1>País: {{ country_name }} ({{ country_code }})</h1>
    <h1>Estado: {{state_name}} ({{state_code}})</h1>
    <h1>Lattiutd: {{latitude}}</h1>
    <h1>Longitud: {{longitude}}</h1>
    <img 
      src="@/assets/city.jpg"
      width="170"
      height="170"
    /> 
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
}


.nombre{
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 2.2em;
}
h1 {
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 1.2em;
}
</style>
