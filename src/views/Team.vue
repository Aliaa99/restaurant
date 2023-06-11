<template>
    <div class="team">
      <div>
        <Hero title="Our Team"/>
      </div>
      <div>
        <HeadAdress title="Team Members"  description="Our Master Chefs "/>
      </div>
      <div>
        <Masterchefs />
      </div>
      <div>
        <Footer />
      </div>
    </div>
  </template>
  <script>
  import Hero from '@/components/Hero.vue'
  import HeadAdress from '@/components/HeadAdress.vue'
  import Masterchefs from '@/components/Masterchefs.vue'
  import Footer from '@/components/Footer.vue'
  export default {
     name: 'services',
     components: {Hero, Masterchefs,HeadAdress ,Footer},
     data: () => ({ 
  
        }),
      }
  </script>
  