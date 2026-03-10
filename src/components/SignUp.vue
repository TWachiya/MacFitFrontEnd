<script setup>
import { ref } from 'vue'

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    emailMatch: () => (`The email and password you entered don't match`),
  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null)

  const confirmPassword = ref(null)
  const show1confirm = ref(false)
</script>

<template>
<v-container width="50%" class="text-center mt-12" style="background-color:#CFD0D6" >
  <v-row>
    <v-col class="mb-12">
    <v-form>
      <v-row>
        <v-col md="12">
          <v-icon color="#3A4B68" icon="mdi-weight-lifter" size="large" class="mt-8"></v-icon>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <div class="text-headline-large font-weight-bold">Sign Up for MacFit Gyms</div>
        </v-col>
      </v-row>
      <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right"> First name</div>
        </v-col>
        <v-col md="6">
          <v-text-field type="Firstname"></v-text-field>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right"> Last name</div>
        </v-col>
        <v-col md="6">
          <v-text-field type="lastname"></v-text-field>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Email</div>
        </v-col>
        <v-col md="6">
          <v-text-field type="email"></v-text-field>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Phone Number</div>
        </v-col>
        <v-col md="6">
          <v-text-field type="tel"></v-text-field>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Gender</div>
        </v-col>
        <v-col md="6">
          <v-radio-group inline>
            <v-radio label="Male" value="male"></v-radio>
            <v-radio label="Female" value="female"></v-radio>
            <v-radio label="Other" value="other"></v-radio>
          </v-radio-group>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Date Of Birth</div>
        </v-col>
        <v-col md="6">
          <v-date-input variant="outlined"></v-date-input>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Gym Location</div>
        </v-col>
        <v-col md="6">
          <v-select
            label="Select Gym Location"
            :items="['Sangale Road', 'Kilimani', 'Westlands', 'Ngong Road']"
            ></v-select>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Password</div>
        </v-col>
        <v-col md="6">
          <v-text-field
                    v-model="password"
                    :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                    :rules="[rules.required, rules.min]"
                    :type="show1 ? 'text' : 'password'"
                    variant="outlined"
                    
                    @click:append="show1 = !show1"
          ></v-text-field>
        </v-col>
        </v-row>
        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Confirm Password</div>
        </v-col>
        <v-col md="6">
          <v-text-field
                    v-model="confirmPassword"
                    :append-icon="show1confirm ? 'mdi-eye' : 'mdi-eye-off'"
                    :rules="[rules.required, rules.min]"
                    :type="show1confirm ? 'text' : 'password'"
                    variant="outlined"
                    
                    @click:append="show1 = !show1"
          ></v-text-field>
        </v-col>
        </v-row>
        <v-row>
          <v-col md="12">
            <v-btn color="#A8BA9A" variant="elevated">Sign Up!</v-btn>
          </v-col>
        </v-row>
        <v-row>
          <v-col md="12">
            <div>New to MacFit? Create an Account</div> 
          </v-col>
        </v-row>
    </v-form>
    </v-col>
  </v-row>
</v-container>
</template>