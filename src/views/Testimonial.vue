<template>
    <div class="team">
      <div>
        <Hero title="Testimonial"/>
      </div>
      <div>
        <HeadAdress title="Testimonial"  description="Our Clients Say!!!"/>
      </div>
      <div>
        <Clients />
      </div>
      <div>
        <Footer />
      </div>
    </div>
  </template>
  <script>
  import Hero from '@/components/Hero.vue'
  import HeadAdress from '@/components/HeadAdress.vue'
  import Clients from '@/components/Clients.vue'
  import Footer from '@/components/Footer.vue'
  export default {
     name: 'services',
     components: {Hero, Clients,HeadAdress ,Footer},
     data: () => ({ 
  
        }),
      }
  </script>
  