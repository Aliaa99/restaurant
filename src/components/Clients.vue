<template>
    <v-container>

    <!-- Make a div wrapped slider,set height and width -->
     <div style="width:100%;margin:20px auto;height:auto">
          <!-- Using the slider component -->
          <slider ref="slider" :options="options">
              <!-- slideritem wrapped package with the components you need -->
              <slideritem v-for="(item,index) in someList" :key="index" class="slide-style" >
                <v-card>
                    <v-icon>{{item.icon}}</v-icon>
                    <p>
                        {{ item.paragraph }}
                    </p>
                    <div class="details">
                      <v-img :src="require('../assets/img/' + item.image  + '.jpg')"></v-img>
                    </div>
                    <div class="details2">
                      <h1>{{ item.name }}</h1>
                      <p>{{item.Profession}}</p>
                    </div>
                </v-card>
            </slideritem>
              <!-- Customizable loading -->
              <div slot="loading">loading...</div>
          </slider>
     </div>

    </v-container>
    </template>
    <script>
    // import slider components
    import { slider, slideritem } from 'vue-concise-slider'
    export default {
        name:'Clients',
       data () {
          return {
            //data list [array]
            someList:[
                {
                icon: 'mdi-format-quote-open',
                paragraph:'Dolor et eos labore, stet justo sed est sed. Diam sed sed dolor stet amet eirmod eos labore diam',
                image:'menu-4',
                name:'Client Name',
                Profession:'Profession'
              },
              {
                icon: 'mdi-format-quote-open',
                paragraph:'Dolor et eos labore, stet justo sed est sed. Diam sed sed dolor stet amet eirmod eos labore diam',
                image:'menu-3',
                name:'Client Name',
                Profession:'Profession'
              },
              {
                icon: 'mdi-format-quote-open',
                paragraph:'Dolor et eos labore, stet justo sed est sed. Diam sed sed dolor stet amet eirmod eos labore diam',
                image:'menu-2',
                name:'Client Name',
                Profession:'Profession'
              },
            ],
            //Slider configuration [obj]
            options: {
                currentPage: 0,
                infinite: 3,
                slidesToScroll: 3,
                loop: true

            }
          }
        },
        components: {
          slider,
          slideritem,
        },
    }
    
    </script>
