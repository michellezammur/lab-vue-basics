<template>
  <!-- // Interaction 2 -->

    <div class="lab">
        <h1>{{stringLab()}}</h1>
    </div>
    <br />
    <br />

    <!-- Interaction 4 -->

    <div v-for="(post, index) in posts" :key="index">
        <ul>
         <li>
           <h3>{{post.title}}</h3>
           <p>{{post.description}}</p>
          <h5>{{post.content}}</h5>
         </li>
        </ul>
    </div>

</template>

<script setup>
import { ref , computed} from "vue";

// <!-- // Interaction 2 -->

const stringLab = () => {
    return "String";
};


// <!-- Interaction 4 -->

const posts = ref([
    {
      title: "Ursus maritimus",
      description: "El oso polar u oso blanco (Ursus maritimus) es una especie de mamífero carnívoro.",
        content: "El oso polar presenta un perfil más alargado que el de otros osos y las patas más desarrolladas, tanto para caminar como para nadar largas distancias.  ",
    },

    {
      title: "Rangifer tarandus",
      description: "El reno, es lo mismo que el ciervo (subespecies euroasiáticas) o caribú (subespecies americanas) (Rangifer tarandus).",
      content:"Los renos o caribúes se encuentran en su rango natural en el norte de Fenoscandia, en Rusia, Groenlandia, Canadá y Alaska. ",
    },

    {
      title: "Spheniscidae",
      description: "Los pingüinos (Spheniscidae) son una familia de aves, la única del orden Sphenisciformes.",
      content:"Los pingüinos son las únicas aves vivientes no voladoras adaptadas al buceo propulsado por las alas.",
    },
    
]);


</script>

<style scoped>



</style>