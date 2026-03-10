<script setup></script>

<template>
  <v-container style="background-color: #A8BA9A" max-width="100%">

    <!-- Centered Title -->
    <v-row justify="center">
      <v-col cols="12" class="text-center">
        <div class="text-display-medium mb-12">Bundles and Pricing</div>
      </v-col>
    </v-row>

    <!-- All Cards in One Container -->
    <v-row justify="center">

      <!-- Daily Pass -->
      <v-col md="3">
        <v-card class="text-center pa-4" >
          <v-icon color="#3A4B68" icon="mdi-arm-flex" size="large" class="mt-8"></v-icon>
          <v-card-title style="color:#3A4B68">Daily Pass</v-card-title>
          <v-card-text>
            Experience the gym on your terms with our Daily Pass.
          </v-card-text>
          <v-card-text class="font-weight-bold">Price: Ksh 500</v-card-text>
        </v-card>
      </v-col>

      <!-- Monthly Pass -->
      <v-col md="3">
        <v-card class="text-center pa-4">
          <v-icon color="#3A4B68" icon="mdi-arm-flex" size="large" class="mt-8"></v-icon>
          <v-card-title style="color:#3A4B68">Monthly Pass</v-card-title>
          <v-card-text>
            Enjoy unlimited access for a full month.
          </v-card-text>
          <v-card-text class="font-weight-bold">Price: Ksh 15000</v-card-text>
        </v-card>
      </v-col>

      <!-- Quarterly Pass -->
      <v-col md="3">
        <v-card class="text-center pa-4" >
          <v-icon color="#3A4B68" icon="mdi-arm-flex" size="large" class="mt-8"></v-icon>
          <v-card-title style="color:#3A4B68">Quarterly Pass</v-card-title>
          <v-card-text>
            Three months of full access.
          </v-card-text>
          <v-card-text class="font-weight-bold">Price: Ksh 45000</v-card-text>
        </v-card>
      </v-col>

      <!-- Half-Yearly Pass -->
      <v-col md="3">
        <v-card class="text-center pa-4" >
          <v-icon color="#3A4B68" icon="mdi-arm-flex" size="large" class="mt-8"></v-icon>
          <v-card-title style="color:#3A4B68">Half-Yearly Pass</v-card-title>
          <v-card-text>
            Six months of commitment and savings.
          </v-card-text>
          <v-card-text class="font-weight-bold">Price: Ksh 90000</v-card-text>
        </v-card>
      </v-col>

      <!-- Yearly Pass -->
      <v-col md="12">
        <v-card class="text-center pa-4">
          <v-icon color="#3A4B68" icon="mdi-dumbbell" size="large" class="mt-8"></v-icon>
          <v-card-title style="color:#3A4B68">Yearly Pass</v-card-title>
          <v-card-text>
            A full year of unlimited access.
          </v-card-text>
          <v-card-text class="font-weight-bold">Price: Ksh 180000</v-card-text>
        </v-card>
      </v-col>

    </v-row>

  </v-container>

   <!-- What's Included -->
     <v-container style="background-color: #A8BA9A" max-width="100%">
        <v-row>
            <v-col md="12">
                <div class="text-display-medium mb-12">What's included in your bundle</div>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="3">
                <v-card>
                    <v-icon color="#3A4B68" icon="mdi-shower-head" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">Steam Rooms and Hot Showers</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card>
                    <v-icon color="#3A4B68" icon="mdi-food-variant" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">Nutritional & Wellness Guidance</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card>
                    <v-icon color="#3A4B68" icon="mdi-dumbbell" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">Personal Training Sessions</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card>
                    <v-icon color="#3A4B68" icon="mdi-clock-check-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">Flexible Scheduling</v-card-title>
                </v-card>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="3">
                <v-card>
                    <v-icon color="#3A4B68" icon="mdi-pool" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">Swimming Pools & Spas</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card>
                    <v-icon color="#3A4B68" icon="mdi-account-group" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">Group Fitness Classes</v-card-title>
                </v-card>
            </v-col>
        </v-row>
     </v-container>

     <!--How to join-->
     <v-container style="background-color: #A8BA9A" max-width="100%">
      <v-row>
        <v-col md="12">
          <div class="text-display-medium mb-12">How to Join</div>
        </v-col>
      </v-row>
      <v-row>
        <v-list>
          <v-list-item>1. Select your preffered gym</v-list-item>
          <v-list-item>2. Fill in an online application</v-list-item>
          <v-list-item>3. Choose your membership bundle</v-list-item>
          <v-list-item>4. Make payment through our secure online portal</v-list-item>
          <v-list-item>5. Receive your digital membership card and welcome package</v-list-item>
        </v-list>
      </v-row>
     </v-container>
</template>