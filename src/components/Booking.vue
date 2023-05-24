<template>
    <div>
      <div class="booking">
          <div class="video">
              <v-btn  @click="dialog = true">
                  <v-icon>mdi-play</v-icon>
              </v-btn>
              <v-dialog
              v-model="dialog"
              width="50%"
              >
                  <iframe width="100%" height="500" :src="result" title="٤ أشياء ستغير حياتك ١٨٠ درجة تمنيت لو نصحني بها أحد من سنين بودكاست ياسر الحزيمي" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>               
              </v-dialog>
          </div>
          <div class="booking-form">
              <h5>
                reservation
              </h5>
              <h1>
              Book A Table Online
              </h1>
              <!-- form -->
              <v-form>
                <v-container>
                <v-row>
                  <!-- name -->
                  <v-col sm="6">
                    <v-text-field
                      v-model="name"
                      :rules="nameRules"
                      :counter="10"
                      label="Your Name"
                      required
                    ></v-text-field>
                  </v-col>
                  <!-- email -->
                  <v-col sm="6">
                    <v-text-field
                      v-model="email"
                      :rules="emailRules"
                      :counter="10"
                      label="Your Email"
                      required
                    ></v-text-field>
                  </v-col>
                  <!-- date -->
                  <v-col cols="6">
                    <v-dialog
                      ref="dialog"
                      v-model="modal"
                      :return-value.sync="date"
                      persistent
                      width="290px"
                    >
                      <template v-slot:activator="{ on, attrs }">
                        <v-text-field
                          v-model="date"
                          label="Date"
                          prepend-icon="mdi-calendar"
                          readonly
                          v-bind="attrs"
                          v-on="on"
                        ></v-text-field>
                      </template>
                      <v-date-picker
                        v-model="date"
                        scrollable
                      >
                        <v-spacer></v-spacer>
                        <v-btn
                          text
                          color="primary"
                          @click="modal = false"
                        >
                          Cancel
                        </v-btn>
                        <v-btn
                          text
                          color="primary"
                          @click="$refs.dialog.save(date)"
                        >
                          OK
                        </v-btn>
                      </v-date-picker>
                    </v-dialog>
                  
                  </v-col>
                  <!-- select number of pepole -->
                  <v-col
                    class="d-flex"
                    cols="6"
                  >
                  <div>
                    <v-select
                      label="No Pepole"
                      :items="this.y"
                      variant="outlined"
                    ></v-select>
                  </div>
                  </v-col>
                  <!-- Textarea -->                            
                  <v-col sm="12" cols="12">
                    <v-textarea label="Label" rows="3"></v-textarea>
                  </v-col>
                  <!-- booking btn -->
                  <v-col cols="12">
                    <v-btn class="general-btn" width="100%">Book Now</v-btn>
                  </v-col>
                </v-row>
              </v-container>
              </v-form>
          </div>
      </div>
    </div>
</template>
<script>

export default{
    name:'Booking',
    data: ()=>({
        result:'https://www.youtube.com/embed/r0S0BU7WGAk',
        dialog: false,
      date: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10),
      menu: false,
      modal: false,
      menu2: false,
      valid: false,
      name:'',
      nameRules: [
        v => !!v || 'Name is required',
        v => v.length <= 10 || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
      y: ['1', '2'],

    }),

}
</script>