<template>
   <div>
    <div class="bg-hero">
        <v-container>
           <v-row cols="6">
              <v-col>
                 <h1>
                    Enjoy Our Delicious Meal
                 </h1>
                 <p>
                    Tempor erat elitr rebum at clita. Diam dolor diam ipsum sit. Aliqu diam amet diam et eos. Clita erat ipsum et lorem et sit, sed stet lorem sit clita duo justo magna dolore erat amet
                 </p>
                 <v-btn class="general-btn">
                    Book A Table
                 </v-btn>
              </v-col>
              <v-col>
                <img src="../assets/img/hero.png">
              </v-col>
           </v-row>
        </v-container>
   </div>
   <!-- options -->
   <div style="padding: 2rem 10px;">
    <Options />
   </div>
   <!-- about -->
   <div>
      <About />
   </div>
</div>
</template>
<script>
import Options from '@/components/Options.vue'
import About from '@/components/About.vue'
export default {
   name: 'Home',
   components: { Options ,About },

    }
</script>
<style scoped lang="scss">
</style>