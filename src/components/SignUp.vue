<script setup>
import { ref } from 'vue'
import { useRouter } from "vue-router";
import { useAuth } from '../services/auth'

const router = useRouter();
const { register, loading, error } = useAuth()

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    passwordMatch: () => password.value === confirmPassword.value || 'Passwords must match'

  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null)

  const confirmPassword = ref(null)
  const show1confirm = ref(false)

  //models
  const firstName = ref(null)
  const lastName = ref(null)
  const email = ref(null)
  const phoneNumber = ref(null)
  const gender = ref(null)
  const dateOfBirth = ref(null)
  const gymLocation = ref(null)

const signUp = async () => {

    loading.value = true;
    error.value = "";

    const formData = new FormData();
    formData.append("name", firstName.value +' '+ lastName.value,);
    formData.append("email", email.value);
    formData.append("phoneNumber", phoneNumber.value);
    formData.append("dob", dateOfBirth.value);
    formData.append("gender", gender.value);
    formData.append("gymLocation", gymLocation.value);
    formData.append("password", password.value);
    formData.append("role_id", 4);

    try {
        await register(formData)
    
        // Redirect after successful signup
        router.push('/homepage').then(() => {
            router.go(0); // Reloads the current route
        });
    } catch (err) {
        // Error is already handled by the auth service
        console.error('Sign up failed', err)
    }
};

</script>

<template>
<v-container width="50%" class="text-center mt-12" style="background: #CFD0D6" >
  <v-row>
    <v-col class="mb-12">
    <v-form>
      <v-row>
        <v-col md="12">
          <v-img src="Macfit.png" width="60%" height="60%"></v-img>
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
          <v-text-field variant="outlined" v-model="firstName"></v-text-field>
        </v-col>
        </v-row>


        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right"> Last name</div>
        </v-col>
        <v-col md="6">
          <v-text-field variant="outlined" v-model="lastName"></v-text-field>
        </v-col>
        </v-row>


        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Email</div>
        </v-col>
        <v-col md="6">
          <v-text-field variant="outlined" v-model="email"></v-text-field>
        </v-col>
        </v-row>


        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Phone Number</div>
        </v-col>
        <v-col md="6">
          <v-text-field  variant="outlined" v-model="phoneNumber" type="number"></v-text-field>
        </v-col>
        </v-row>


        <v-row>
        <v-col md="6">
          <div class="text-title-medium font weight medium text-right">Gender</div>
        </v-col>
        <v-col md="6">
          <v-radio-group inline variant="outlined" v-model="gender" >
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
          <v-date-input  variant="outlined" v-model="dateOfBirth" label="Date input"></v-date-input>
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
                    :rules="[rules.required, rules.min, rules.passwordMatch,]"
                    :type="show1confirm ? 'text' : 'password'"
                    variant="outlined"
                    
                    @click:append="show1confirm = !show1confirm"
          ></v-text-field>
        </v-col>
        </v-row>


        <v-row>
          <v-col md="12">
            <v-btn color="#A8BA9A" variant="elevated" @click="signUp">Sign Up!</v-btn>
          </v-col>
        </v-row>


        <v-row>
          <v-col md="12">
            <div>Already have an account? 
              <router-link to="/login"> Log in</router-link>
            </div> 
          </v-col>
        </v-row>


    </v-form>
    </v-col>
  </v-row>
</v-container>
</template>