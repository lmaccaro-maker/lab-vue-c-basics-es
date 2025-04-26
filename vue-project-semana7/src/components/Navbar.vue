<script setup>
function sum() {
  return 2 + 2;
}

import { ref } from "vue";

const isVisible = ref(true);

// Método para alternar el valor de isVisible
function toggleVisibility() {
  isVisible.value = !isVisible.value;
}

// Crea una variable booleana reactiva para controlar el estilo
const isHighlighted = ref(false);

// Método para alternar el valor de la variable booleana
function toggleHighlight() {
  isHighlighted.value = !isHighlighted.value;
}
</script>

<template>
  <div>
    <p>El resultado de 2 + 2 es: {{ sum() }}</p>
  </div>

  <div>
    <!-- Elemento que se muestra solo si `isVisible` es true -->
    <p v-if="isVisible">Este elemento se muestra porque isVisible es true.</p>
    <!-- Botón para cambiar el valor de isVisible -->
    <button @click="toggleVisibility">Toggle Visibility</button>

    <div>
      <h1 :class="{ highlighted: isHighlighted }">
        Presiona el botón para cambiar mi color de fondo
      </h1>
      <button @click="toggleHighlight">Cambiar Color</button>
    </div>
  </div>
</template>

<style>
.highlighted {
  background-color: rgb(233, 93, 23);
  padding: 10px;
}
</style>
