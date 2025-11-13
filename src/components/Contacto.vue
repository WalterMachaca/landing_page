<template>
  <section class="gradient-bg text-white py-20">
    <div class="container mx-auto px-6 text-center">
      <h3 class="text-4xl font-bold mb-6">
        ¿Quieres saber más sobre automatización de un sistema de riego?
      </h3>
      <p class="text-xl mb-8 max-w-2xl mx-auto">
        Únete a cientos de usuarios que ya disfrutan de un sistema inteligente y eficiente.
      </p>
      <button @click="info"
        class="bg-white text-blue-600 px-8 py-4 rounded-lg font-semibold text-lg hover:bg-blue-50 transition-colors">
        Solicitar Información
      </button>
    </div>
  </section>
</template>

<script setup>
function info() {
  alert('¡Gracias por tu interés! Te contactaremos pronto con más detalles sobre AquaBot.');
}
</script>
