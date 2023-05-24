<template>
    <div class="masterchefs">
        <v-container>
            <v-row>
                <v-col cols="3" v-for="item in items" :key="item.id">
                    <v-card>
                        <v-img  />
                        <h3>{{name}}</h3>
                        <p>{{description}}</p>
                        <div>
                            <v-icon>mdi-{{icon1}}</v-icon>
                            <v-icon>mdi-{{icon2}}</v-icon>
                            <v-icon>mdi-{{icon3}}</v-icon>
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
            {image:'../assets/img/team-1.jpg',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'},
            {image:'../assets/img/team-1.jpg',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'},
            {image:'../assets/img/team-1.jpg',name:'Full Name',description:'description',icon1:'facebook',icon2:'twitter',icon3:'instagram'}
        ]
    })

   }
</script>