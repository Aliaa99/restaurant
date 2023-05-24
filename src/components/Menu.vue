<template>
    <v-container>
      <div>  
        <v-tabs
            v-model="tab">
            <v-tab
            v-for="item in items"
            :key="item.id"
            class="tabstyle"
            >
              <div v-for="newtab in item.tab" :key="newtab.id">
                <v-row>
                    <v-col cols="4">
                       <v-icon>{{newtab.icon}}</v-icon>
                    </v-col>
                    <v-col cols="8">
                       <h4><span>{{ newtab.desc }}</span>{{ newtab.name}}</h4>
                    </v-col>
                </v-row>
              </div>
            </v-tab>
        </v-tabs>
    
        <v-tabs-items v-model="tab">
            <v-tab-item
            v-for="item in items"
            :key="item.id"
            class="tabitem"
            >
            <div >
                <v-row>
                  <v-col cols="6" v-for="newitem in item.content" :key="newitem.id">
                    <v-row>
                        <v-col cols="2">
                            <img :src="require('../assets/img/'+ newitem.image +'.jpg')" /> 
                        </v-col>
                        <v-col cols="10">
                            <h2>{{newitem.title}} <span>{{newitem.price}}</span></h2>
                            <p>{{ newitem.text }}</p>
                        </v-col>
                    </v-row>
                    </v-col>
                </v-row>
            </div>
            </v-tab-item>
        </v-tabs-items>
      </div>
    </v-container>  
  </template>
  
  <script>
    export default {
    name: 'Menu',
    data: () => ({
        tab: null,
        items: [
          { tab: [
                  {name:'Breakfast',desc:'popular',icon:'mdi-coffee'},
               ],
            content: [
                    {image:'menu' ,title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    {image:'menu-4',title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    {image:'menu-5',title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    ] 
          },
                    { tab: [
                  {name:'Lunch',desc:'special',icon:'mdi-food'},
               ],
            content: [
                    {image:'menu' ,title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    {image:'menu-4',title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    {image:'menu-5',title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    ] 
          },
          { tab: [
                  {name:'Dinner',desc:'lovely',icon:'mdi-silverware-fork-knife'},
               ],
            content: [
                    {image:'menu' ,title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    {image:'menu-4',title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    {image:'menu-5',title:'Chicken Burger',price:'125',text:'Ipsum ipsum clita erat amet dolor justo diam'},
                    ] 
          },

        ],
    }),

    }
</script>













