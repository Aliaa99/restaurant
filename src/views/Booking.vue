<template>
    <div class="booking">
      <div>
        <Hero title="Booking"/>
      </div>
      <div>
        <Booking />
      </div>
      <div>
        <Footer />
      </div>
    </div>
  </template>
  <script>
  import Hero from '@/components/Hero.vue'
  import Booking from '@/components/Booking.vue'
  import Footer from '@/components/Footer.vue'
  export default {
     name: 'services',
     components: {Hero, Booking ,Footer},
     data: () => ({ 
  
        }),
      }
  </script>
  