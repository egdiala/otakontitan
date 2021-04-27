<template>
  <v-container class="booking d-flex justify-center d-flex align-center">
    <v-row>
      <v-col class="mx-auto" cols="12" xl="10" lg="10" md="3" sm="3">
        <v-form ref="form"
    v-model="valid"
    lazy-validation @submit="submit">
          <v-text-field
            v-model.trim="name" :rules="nameRules" outlined
            label="Name"
          ></v-text-field>
          <v-text-field
            v-model.trim="email" :rules="emailRules" type="email" outlined
            label="E-mail"
            required
          ></v-text-field>
        <p class="text-center mb-5"><small>By booking a ticket online for the OtakonTitan Convention, you agree to pay a sum of</small> <strong>₦300</strong>.</p>
              <v-btn
            block color="#e73c7e" class="text-capitalize" :loading="loading"
            @click.prevent="submit"
          >
            Book Now
          </v-btn>
        </v-form>        
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import axios from 'axios';
export default {
    name: 'Booking',
    data() {
      return {
        loading: false,
        valid: false,
        name: '',
        nameRules: [
          v => !!v || 'Name is required',
        ],
        email: '',
        emailRules: [
          v => !!v || 'E-mail is required',
          v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
        ],
      }
    },
    methods: {
      submit() {
        this.validate();
        setTimeout(() => {
          if (this.valid) {
              this.loading = true;
            axios.get(`https://otakon-api.herokuapp.com/book?name=${this.name}&email=${this.email}`).then(res => {
              this.loading = false;
              console.log(res);
            }).catch(err => {
              this.loading = false;
              console.log(err);
            })          
          }          
        }, 300);
      },
      validate () {
        this.$refs.form.validate();
      },
    },
}
</script>

<style scoped>
.booking {
  height: 100%;
}
</style>
