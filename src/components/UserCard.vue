<template>
  <div class="user-card">
    <div class="card-header">
      <img :src="props.foto" :alt="props.nombre" class="foto" />
    </div>

    <div class="card-body">
      <h2 class="user-nombre">{{ props.nombre }}</h2>
      <p class="user-actividad">{{ props.actividad }}</p>
      <hr class="divider" />
      <p class="user-descripcion">{{ props.descripcion }}</p>
    </div>
  </div>
</template>

<script setup>
// Manejo de propiedades (Props)
const props = defineProps({
  nombre: {
    type: String,
    required: true
  },
  actividad: {
    type: String,
    required: true
  },
  descripcion: {
    type: String,
    required: true
  },
  foto: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.user-card {
  width: 300px;
  margin: 2rem auto;
  background-color: #ffffff;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
  border: 1px solid #4b0000;
}

.card-header {
  background-color: #f8f9fa;
  padding: 2rem 0 1rem;
  display: flex;
  justify-content: center;
}

.foto {
  width: 100px;
  height: 100px;
  object-fit: cover;
  border: 1px solid #4b0000;
}

.card-body {
  padding: 1.5rem;
  text-align: center;
}

.user-nombre {
  margin: 0;
  font-size: 1.25rem;
  color: #2c3e50;
  font-weight: 700;
}

.user-actividad {
  margin: 0.4rem 0;
  font-size: 0.85rem;
  color: #4b0000;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.divider {
  border: 0;
  border-top: 1px solid #eee;
  width: 40%;
}

.user-descripcion {
  font-size: 0.95rem;
  color: #5e6d82;
  line-height: 1.6;
}
</style>