<template>
    <div class="contact">
      <div>
        <Hero title="Contact Us "/>
      </div>
      <div>
        <Head-Adress title="Contact Us"  description="Contact For Any Query "/>
      </div>
      <div>
        <Contact />
      </div>
      <div>
        <Footer />
      </div>
    </div>
  </template>
  <script>
  import Hero from '@/components/Hero.vue'
  import HeadAdress from '@/components/HeadAdress.vue'
  import Contact from '@/components/Contact.vue'
  import Footer from '@/components/Footer.vue'
  export default {
     name: 'services',
     components: {Hero, Contact ,HeadAdress, Footer},
     data: () => ({ 
  
        }),
      }
  </script>
  