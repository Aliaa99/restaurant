<template>
    <div class="services">
      <div>
        <Hero title="Services "/>
      </div>
      <div>
        <Head-Adress title="Our Services"  description="Explore Our Services "/>
      </div>
      <div>
        <options />
      </div>
      <div>
        <Footer />
      </div>
    </div>
  </template>
  <script>
  import Hero from '@/components/Hero.vue'
  import HeadAdress from '@/components/HeadAdress.vue'
  import Options from '@/components/Options.vue'
  import Footer from '@/components/Footer.vue'
  export default {
     name: 'services',
     components: {Hero, Options ,HeadAdress, Footer},
     data: () => ({ 
  
        }),
      }
  </script>
  