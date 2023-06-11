<template>
  <div class="about">
    <div>
      <Hero title="About Us"/>
    </div>
    <div>
      <About />
    </div>
    <div>
      <Head-Adress title="Team Members"  description="Our Master Chefs"/>
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
import About from '@/components/About.vue'
import HeadAdress from '@/components/HeadAdress.vue'
import Masterchefs from '@/components/Masterchefs.vue'
import Footer from '@/components/Footer.vue'
export default {
   name: 'AboutView',
   components: {Hero, About ,HeadAdress, Masterchefs, Footer},
   data: () => ({ 

      }),
    }
</script>
