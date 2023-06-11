<template>
    <div class="services">
      <div>
        <Hero title="Food Menu "/>
      </div>
      <div>
        <Head-Adress title="Food Menu"  description="Most Popular Items  "/>
      </div>
      <div>
        <Menu />
      </div>
      <div>
        <Footer />
      </div>
    </div>
  </template>
  <script>
  import Hero from '@/components/Hero.vue'
  import HeadAdress from '@/components/HeadAdress.vue'
  import Menu from '@/components/Menu.vue'
  import Footer from '@/components/Footer.vue'
  export default {
     name: 'services',
     components: {Hero, Menu ,HeadAdress,Footer},
     data: () => ({ 
  
        }),
      }
  </script>
  