<template>
    <div class="bg-hero">
        <v-container>
           <v-row cols="12">
              <v-col>
                 <h1 style="text-align: center;">
                    {{title}}
                 </h1>
              </v-col>
           </v-row>
        </v-container>
   </div>

</template>
<script>
  export default{
    name:'Hero',
    props: {
      title: {
         type: String,
         default: ''
      }
    },
   
  }
</script>