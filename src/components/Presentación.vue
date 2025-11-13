<template>
  <section id="inicio" class="gradient-bg text-white py-20">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-5xl font-bold mb-6">Riego Inteligente con Arduino</h2>
      <p class="text-xl mb-8 max-w-2xl mx-auto">
        Automatiza el cuidado de tus plantas con tecnología avanzada.
        Sensores de humedad y temperatura, control remoto y eficiencia energética.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <button @click="demo" class="bg-white text-blue-600 px-8 py-3 rounded-lg font-semibold hover:bg-blue-50">
          Ver Demo
        </button>
        <button @click="info" class="border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-blue-600">
          Más Información
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
function demo() {
  alert('¡Demo del sistema de riego! Aquí podrías ver una simulación en tiempo real.');
}

function info() {
  alert('¡Gracias por tu interés! Te contactaremos pronto con más detalles sobre AquaBot.');
}
</script>