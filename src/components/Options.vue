<template>
    <v-container >
    <v-row >
      <v-col cols="3"  v-for="item in items" :key="item.id">
            <v-card class="options" >
                <v-icon class="options-icon">{{ item.icon }}</v-icon>
                <h3 class="options-h">{{ item.name }}</h3>        
                <v-card-text class="options-text">
                    {{ item.paragraph }}
                </v-card-text>
            </v-card>

    </v-col>
    </v-row>
    </v-container>
  </template>
  <script>
    export default {
    name: 'Options',
    data: () => ({
        items:[
            {name:'master chef' , icon:'mdi-account-tie' , paragraph:'Diam elitr kasd sed at elitr sed ipsum justo dolor sed clita amet diam'},
            {name:'Quality Food' , icon:'mdi-food' , paragraph:'Diam elitr kasd sed at elitr sed ipsum justo dolor sed clita amet diam'},
            {name:'Online Order' , icon:'mdi-cart-plus' , paragraph:'Diam elitr kasd sed at elitr sed ipsum justo dolor sed clita amet diam'},
            {name:'24/7 Service' , icon:'mdi-headset' , paragraph:'Diam elitr kasd sed at elitr sed ipsum justo dolor sed clita amet diam'},
        ]
    
    })
    }

  </script>