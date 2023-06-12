<template>
    <div>
        <v-container>
           <v-row>
             <v-col sm="4" cols="12">
                <div class="contact">
                    <div class="contact-title">
                        Booking
                    </div>
                    <div class="contact-info">
                        <v-icon>mdi-email</v-icon>
                        book@example.com
                    </div>
                </div>
             </v-col>
             <v-col sm="4" cols="12">
                <div class="contact">
                    <div class="contact-title">
                        General
                    </div>
                    <div class="contact-info">
                        <v-icon>mdi-email</v-icon>
                        info@example.com
                    </div>
                </div>
             </v-col>
             <v-col sm="4" cols="12">
                <div class="contact">
                    <div class="contact-title">
                        Technical
                    </div>
                    <div class="contact-info">
                        <v-icon>mdi-email</v-icon>
                        tech@example.com
                    </div>
                </div>
             </v-col>
           </v-row>

            <v-row>
                <!-- map -->
                <v-col md="6" cols="12">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d43109.46404148012!2d6.139331415419217!3d47.52221401973193!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47928c21dbead7ab%3A0x409ce34b30f0970!2s70230%20Filain!5e0!3m2!1sen!2sfr!4v1640189073328!5m2!1sen!2sfr" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </v-col>
                <!-- form -->
                <v-col md="6" cols="12">
                    <v-form class="contact-form">
                        <v-row>
                            <v-col cols="6" style="max-height: 70px;">
                                <v-text-field
                                v-model="name"
                                :counter="10"
                                :rules="nameRules"
                                label="Name"
                                required
                              ></v-text-field>
                            </v-col>
                            <v-col cols="6" style="max-height: 70px;">
                                <v-text-field
                                v-model="email"
                                :counter="10"
                                :rules="emailRules"
                                label="Email"
                                required
                              ></v-text-field>
                            </v-col>
                            <v-col sm="12" cols="12" style="max-height: 70px;" >
                                <v-textarea label="subject" rows="2"></v-textarea>
                              </v-col>
                              <v-col sm="12" cols="12" >
                                <v-textarea label="message" rows="4"></v-textarea>
                              </v-col>
                              <!-- booking btn -->
                              <v-col cols="12">
                                <v-btn class="general-btn" width="100%">Send Message</v-btn>
                              </v-col>            
                        </v-row>
                    </v-form>
                </v-col>
            </v-row>
        </v-container>    
    </div>
</template>
<script>
export default{
    name:'contact',
    data:() =>({
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

    })
}
</script>