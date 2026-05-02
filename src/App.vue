<script setup>
import { ref } from 'vue'
import UserCard from './components/UserCard.vue'

const nombre = ref('Muhamad Ali')
const actividad = ref('Boxeador')
const descripcion = ref('Un boxeador y activista político.')
const foto = ref('https://i.pinimg.com/736x/ee/25/de/ee25deed6a34e7ecef7fd21248fa6457.jpg')
</script>

<template>
  <div>
    <input v-model="nombre" placeholder="Nombre" />
    <input v-model="actividad" placeholder="Actividad" />
    <input v-model="descripcion" placeholder="Descripción" />
    <input v-model="foto" placeholder="URL de la foto" />

    <UserCard
      :nombre="nombre"
      :actividad="actividad"
      :descripcion="descripcion"
      :foto="foto"
    />
  </div>
</template>