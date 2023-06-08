<template>
    <div class="masterchefs">
        <v-container>
            <v-row>
                <v-col md="3" sm="6" xs="6" v-for="item in items" :key="item.id">
                    <v-card>
                        <div>
                            <v-img :src="require('../assets/img/'+ item.image +'.jpg')" />
                        </div>
                        <h3>{{item.name}}</h3>
                        <p>{{item.description}}</p>
                        <div class="social">
                           <v-btn><v-icon>mdi-{{item.icon1}}</v-icon></v-btn> 
                           <v-btn><v-icon>mdi-{{item.icon2}}</v-icon></v-btn> 
                           <v-btn><v-icon>mdi-{{item.icon3}}</v-icon></v-btn> 
                        </div>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>
<script>
   export default{
    name:'Masterchefs',
    data: () => ({
        items:[
            {image:'team-1',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'},
            {image:'team-2',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'},
            {image:'team-3',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'},
            {image:'team-4',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'}
        ]
    })

   }
</script>