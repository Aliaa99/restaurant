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
    <style lang="scss">
    .slide-style{
        width: 30%;
        margin: 10px;
        .v-card{
            padding: 15px;
            text-align: left;
            .v-icon{
                color: orange;
                font-size: 3rem;
            }
            .details{
              display: inline-block;
              .v-image{
                  border-radius: 50% !important;
                  width: 60px !important;
                  height: 60px !important;
              }
            }
            p{
                font-size: 15px;
                color:gray;
            }
            .details2{
              display: inline-block;
              line-height: 40px;
                h1{
                  font-size: 20px;
                  margin-bottom: 5px;
                  padding: 5px;
                }
                p{
                  padding: 0px 5px;
                  line-height: 5px;
                }
            }
       }
    }
    .slider-pagination{
      position: relative !important;
      padding: 10px;
   }
   .slider-pagination-bullet{
      width: 20px !important;
      height: 20px !important;
   }
   .slider-pagination-bullet-active{
      background-color: orange !important;
   }
    </style>