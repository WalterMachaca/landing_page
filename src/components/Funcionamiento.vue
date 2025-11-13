<template>
  <section id="como-funciona" class="py-20 bg-gray-50">
    <div class="container mx-auto px-6">
      <h3 class="text-4xl font-bold text-center text-gray-800 mb-16">¿Cómo Funciona?</h3>
      <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-12 items-center">
        <div class="space-y-8">
          <div v-for="(step, i) in steps" :key="i" class="flex items-start space-x-4">
            <div class="w-8 h-8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold">
              {{ i + 1 }}
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-800 mb-2">{{ step.title }}</h4>
              <p class="text-gray-600">{{ step.text }}</p>
            </div>
          </div>
        </div>
        <div class="bg-white p-8 rounded-xl shadow-lg text-center">
          <div class="w-32 h-32 bg-gradient-to-br from-blue-400 to-green-400 rounded-full mx-auto mb-6"></div>
          <h4 class="text-xl font-semibold text-gray-800 mb-4">Sistema Arduino</h4>
          <p class="text-gray-600 mb-6">Microcontrolador programado para gestión inteligente del riego</p>
          <div class="grid grid-cols-2 gap-4 text-sm">
            <div class="bg-blue-50 p-3 rounded-lg font-semibold text-blue-800">Sensores</div>
            <div class="bg-green-50 p-3 rounded-lg font-semibold text-green-800">Bomba</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  { title: 'Detección de Humedad', text: 'El sensor DHT11 mide la humedad y temperatura del ambiente constantemente.' },
  { title: 'Procesamiento Inteligente', text: 'La placa Arduino analiza los datos y determina el momento del riego.' },
  { title: 'Riego Automático', text: 'La mini bomba se activa automáticamente según la necesidad.' }
]
</script>
