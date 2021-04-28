<template>
    <v-container class="done d-flex justify-center d-flex align-center">
        <v-row>
            <v-col class="mx-auto text-center" cols="12" xl="10" lg="10" md="3" sm="3">
                <div class="checkmark-box mx-auto">
                    <i class="mr-4">✓</i>
                </div>
                <h1>Success</h1> 
                <p>We received your payment.<br/> Kindly check your email for a QR Code.</p>          
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'Success',
    data() {
      return {
      }
    },
    methods: {
    },
}
</script>
<style scoped>
.done {
  height: 100%;
}
.checkmark-box {
    border-radius:50%; 
    height:200px; 
    width:200px; 
    background: #f5ffe6;
}
i {
    color: #9ABC66;
    font-size: 100px;
    line-height: 200px;
}
p {
    color: #404F5E;
    font-family: "Nunito Sans", "Helvetica Neue", sans-serif;
    font-size:20px;
    margin: 0;
}
h1 {
    color: #88B04B;
    font-family: "Nunito Sans", "Helvetica Neue", sans-serif;
    font-weight: 900;
    font-size: 40px;
    margin-bottom: 10px;
}
</style>