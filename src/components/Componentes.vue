<template>
  <section id="caracteristicas" class="py-20 bg-white">
    <div class="container mx-auto px-6">
      <h3 class="text-4xl font-bold text-center text-gray-800 mb-16">Componentes</h3>
      <div class="grid md:grid-cols-3 gap-8">
        <div v-for="(item, index) in features" :key="index"
             class="bg-white p-8 rounded-xl shadow-lg border border-gray-100 transition-transform hover:scale-105">
          <img :src="item.img" class="mx-auto mb-4 rounded-lg" alt="">
          <h4 class="text-xl font-semibold text-gray-800 mb-4 text-center">{{ item.title }}</h4>
          <p class="text-gray-600 text-center">{{ item.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    img: '/src/assets/sensorDHT11.PNG',
    title: 'Sensor de Humedad y Temperatura DHT11',
    text: 'Monitoreo en tiempo real de la temperatura y humedad del ambiente para un riego preciso y eficiente.'
  },
  {
    img: '/src/assets/módulobluetooth.PNG',
    title: 'Módulo Bluetooth HC-05',
    text: 'Programa tu sistema desde cualquier lugar. Módulo tipo Bluetooth 2.0 compatible con Smartphones Android y PC.'
  },
  {
    img: '/src/assets/arduinoUNO.PNG',
    title: 'Arduino Uno',
    text: 'Placa de microcontrolador de código abierto. Diseño optimizado con componentes de bajo consumo.'
  },
  {
    img: '/src/assets/LCD 16x2 I2C.jpg',
    title: 'Pantalla LCD 16x2 I2C',
    text: 'Dispositivo empleado para la visualización de contenido, mediante caracteres o símbolos, dispone de 2 filas de 16 caracteres cada una.'
  },
  {
    img: '/src/assets/minibomba.jpg',
    title: 'Mini Bomba de Agua',
    text: 'Dispositivo compacto sumergible con alimentación de 5V. Es de bajo consumo energético y se pueden controlar mediante microcontroladores.'
  },
  {
    img: '/src/assets/Protoboard.jpg',
    title: 'Protoboard',
    text: 'Placa de pruebas sin soldadura que permite construir y probar circuitos electrónicos de manera rápida y sencilla.'
  }

]
</script>
