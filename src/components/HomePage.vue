<script setup>
import { ref } from 'vue'

const userName = ref('User') // Placeholder string, would ideally come from user auth state
const activeStreak = ref(12)
const upcomingClass = ref({ name: 'HIIT Core', time: '17:30', instructor: 'Sarah M.' })
const recentActivity = ref([
  { title: 'Strength Training', date: 'Today, 08:00 AM', icon: 'mdi-weight-lifter', color: '#1FD204' },
  { title: 'Cardio Session', date: 'Yesterday, 06:30 PM', icon: 'mdi-run', color: '#3A4B68' },
  { title: 'Yoga Flow', date: 'Mon, 07:00 AM', icon: 'mdi-yoga', color: 'info' }
])

</script>

<template>
  <v-container class="px-6 py-8 bg-surface" fluid>
    <!-- Welcome Header -->
    <v-row class="mb-6">
      <v-col cols="12">
        <v-card 
          class="welcome-card rounded-xl text-white pa-8" 
          elevation="4"
          image="/Landscape1.jpg"
          theme="dark"
        >
          <div class="overlay"></div>
          <div class="content">
             <div class="text-h3 font-weight-bold mb-2">Welcome back, {{userName}}!</div>
             <div class="text-h6 font-weight-regular text-medium-emphasis text-white mb-6">Ready to crush your goals today?</div>
             <v-btn color="#1FD204" size="large" rounded="pill" elevation="2" class="font-weight-bold">
               START WORKOUT
             </v-btn>
          </div>
        </v-card>
      </v-col>
    </v-row>

    <!-- Quick Stats -->
    <v-row class="mb-6">
      <v-col cols="12" md="4">
         <v-card class="rounded-xl pa-5 h-100 stat-card" elevation="2">
           <div class="d-flex align-center justify-space-between mb-2">
             <div class="text-overline text-medium-emphasis font-weight-bold">Active Streak</div>
             <v-icon  size="large">mdi-fire</v-icon>
           </div>
           <div class="d-flex align-baseline gap-2">
             <div class="text-h3 font-weight-bold text-grey-darken-4">{{ activeStreak }}</div>
             <div class="text-subtitle-1 text-medium-emphasis font-weight-medium">days</div>
           </div>
           <v-progress-linear class="mt-4" model-value="80" color="#1FD204" rounded height="8"></v-progress-linear>
         </v-card>
      </v-col>
      
      <v-col cols="12" md="4">
         <v-card class="rounded-xl pa-5 h-100 stat-card" elevation="2">
           <div class="d-flex align-center justify-space-between mb-4">
             <div class="text-overline text-medium-emphasis font-weight-bold">Next Class</div>
             <v-icon color="#3A4B68" size="large">mdi-calendar-clock</v-icon>
           </div>
           <div class="text-h5 font-weight-bold mb-1 text-grey-darken-4">{{ upcomingClass.name }}</div>
           <div class="text-body-1 text-medium-emphasis d-flex align-center gap-2 mb-1">
             <v-icon size="small">mdi-clock-outline</v-icon> {{ upcomingClass.time }}
           </div>
           <div class="text-body-2 text-medium-emphasis">with {{ upcomingClass.instructor }}</div>
         </v-card>
      </v-col>

          </v-row>

    <!-- Lower Section: Activity & Actions -->
    <v-row>
      <!-- Quick Actions Grid -->
      <v-col cols="12" md="7">
        <div class="text-h5 font-weight-bold mb-4 px-2 text-primary-dark">Quick Actions</div>
        <v-row>
           <v-col cols="6" sm="4">
              <v-card class="action-card rounded-xl text-center pa-6" elevation="2" to="/gym-locations" hover>
                <div class="icon-wrapper bg-green-lighten-5 rounded-circle mx-auto mb-4 d-flex align-center justify-center">
                  <v-icon size="36" color="#1FD204">mdi-map-marker-radius</v-icon>
                </div>
                <div class="text-button font-weight-bold text-grey-darken-3">Find Gym</div>
              </v-card>
           </v-col>
           <v-col cols="6" sm="4">
              <v-card class="action-card rounded-xl text-center pa-6" elevation="2" to="/bundles" hover>
                <div class="icon-wrapper bg-blue-grey-lighten-5 rounded-circle mx-auto mb-4 d-flex align-center justify-center">
                  <v-icon size="36" color="#3A4B68">mdi-tag-multiple</v-icon>
                </div>
                <div class="text-button font-weight-bold text-grey-darken-3">Bundles</div>
              </v-card>
           </v-col>
           <v-col cols="6" sm="4">
              <v-card class="action-card rounded-xl text-center pa-6" elevation="2" to="/profile" hover>
                <div class="icon-wrapper bg-light-blue-lighten-5 rounded-circle mx-auto mb-4 d-flex align-center justify-center">
                  <v-icon size="36" color="info">mdi-account-cog</v-icon>
                </div>
                <div class="text-button font-weight-bold text-grey-darken-3">Profile</div>
              </v-card>
           </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
  
</template>

