<script setup>
const userDetails = JSON.parse(localStorage.getItem('userDetails')) 


</script>

<template>
<v-container width="50%" style="background-color:#CFD0D6" class="text-center mt-12" >
  <v-row>
    <v-col>
      <v-card>
         <v-img src="" class="" cover></v-img>
         <v-card-title>{{ userDetails.name }}</v-card-title>
         <v-card-text>{{ userDetails.email }}</v-card-text>
         <v-card-text>{{ userDetails.phoneNumber }}</v-card-text>
         <v-card-text>{{ userDetails.gymLocation }}</v-card-text>
         <v-card-text>Your current subscription is: {{ userDetails.subscription.name}} at {{ userDetails.subscription.price }}</v-card-text>
         <div v-if="userDetails.subscription">
          </div>
          <div v-else>
            <v-btn color="primary" variant="outlined" to="/bundles">Select to a bundle</v-btn>
          </div>
        </v-card>
    </v-col>
  </v-row>
</v-container>
</template>
    