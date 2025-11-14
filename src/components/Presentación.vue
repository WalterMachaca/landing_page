<template>
  <section id="inicio" class="gradient-bg text-white py-20">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-5xl font-bold mb-6">Riego Inteligente con Arduino</h2>
      <p class="text-xl mb-8 max-w-2xl mx-auto">
        Automatiza el cuidado de tus plantas con tecnología avanzada.
        Sensores de humedad y temperatura, control remoto y eficiencia energética.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <video 
          v-if="mostrarVideo"
          ref="videoRef"
          src="/src/assets/demo.mp4" 
          controls 
          autoplay
          class="max-w-xl mx-auto"
        ></video>  
        
        <button @click="mostrarVideo=true" class="bg-white text-blue-600 px-8 py-3 rounded-lg font-semibold hover:bg-blue-50">
          Ver Demo
        </button>
      
      <a href="https://wa.me/+59178731634?text=Hola%20quiero%20más%20informaci%C3%B3n%20sobre%20el%20sistema%20de%20riego" target="_blank">
        <button @click="info" class="border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-blue-600">
          Más Información
        </button>
      </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      mostrarVideo: false,
    };
  },

  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },

  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },

  methods: {
    handleScroll() {
      // Si ya mostró el video y el scroll bajó más de 200px
      if (this.mostrarVideo && window.scrollY > 200) {
        
        // Pausar el video
        const video = this.$refs.videoRef;
        if (video) video.pause();

        // Ocultar el video
        this.mostrarVideo = false;
      }
    }
  }
};
</script>