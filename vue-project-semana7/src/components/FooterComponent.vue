<script setup>
import { ref } from "vue";

// Define la lista de publicaciones usando ref()
const posts = ref([
  {
    titulo: "Primera Publicación",
    descripcion: "Esta es la primera publicación.",
    contenido: "Contenido detallado de la primera publicación.",
  },
  {
    titulo: "Segunda Publicación",
    descripcion: "Descripción de la segunda publicación.",
    contenido: "Aquí está el contenido de la segunda publicación.",
  },
  {
    titulo: "Tercera Publicación",
    descripcion: "Esta es la tercera publicación en la lista.",
    contenido: "Más detalles sobre la tercera publicación.",
  },
]);
</script>

<template>
  <div>
    <h1>Lista de Publicaciones</h1>
    <ul>
      <li v-for="(post, index) in posts" :key="index">
        <h2>{{ post.titulo }}</h2>
        <p><strong>Descripción:</strong> {{ post.descripcion }}</p>
        <div>{{ post.contenido }}</div>
      </li>
    </ul>
  </div>
</template>

<style></style>
