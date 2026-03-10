<script setup>

</script>

<template>
  <v-container color="#CFD0D6" max-width=90%>
    <v-row>
      <v-carousel>
        <v-carousel-item src="/Landscape1.jpg"cover></v-carousel-item>>
        <v-carousel-item src="/Landscape2.jpg"cover></v-carousel-item>>
        <v-carousel-item src="/Landscape.jpg"cover></v-carousel-item>>
      </v-carousel>
    </v-row>
  </v-container>
 <!-- About Us -->
     <v-container style="background-color: #CFD0D6;" max-width="100%">
        <v-row >
            <v-col md="8" class="text-center">
                <div class="text-display-medium mb-12">Welcome to MacFit Gyms</div>
                <div class="text-title-large font-weight-light text-medium emphasis mb-8 ">At MacFit, we believe fitness should be accessible, personalized, and empowering for everyone. Our platform was built with a simple mission: to help people move with confidence, stay consistent, and achieve their goals through smart, intuitive technology. Whether you're just starting your fitness journey or pushing toward new performance milestones, we’re here to guide you every step of the way.</div>
                <div class="text-title-large font-weight-light text-medium emphasis mb-8">We combine expert‑designed programs, real‑time progress tracking, and a supportive digital environment to create a training experience that adapts to your lifestyle. Every feature—from workout recommendations to equipment insights—is crafted to help you train smarter, not harder. With MacFit, you’re not just following routines; you’re building sustainable habits backed by data and thoughtful design.</div>
                <div class="text-title-large font-weight-light text-medium emphasis mb-8">Our team is passionate about redefining what fitness can look like in a digital world. We’re constantly innovating, refining, and expanding our tools to ensure you have everything you need to stay motivated and inspired. MacFit isn’t just an app—it’s a community, a coach, and a companion on your path to becoming the strongest version of yourself.</div>
                <v-btn color="#1FD204">LEARN MORE</v-btn>
            </v-col>
            <v-col md="2">
              <v-container class="d-flex align-center justify-center fill-height">
                <v-img src="/Landscape3.jpg"></v-img>
              </v-container>
            </v-col>
        </v-row>
     </v-container>
     <v-container>
        <v-row>
            <v-col md="4">
                <v-card>
                    <v-img src="Square2.jpg" cover></v-img>
                    <v-card-title>1. Strength Training</v-card-title>
                    <v-card-text>Build power. Build confidence.Progressive workouts designed to increase muscle strength, boost endurance, and elevate your overall performance.</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
             <v-col md="4">
                <v-card>
                    <v-img src="Square3.jpg" cover></v-img>
                    <v-card-title>2. Cardio Workouts</v-card-title>
                    <v-card-text>Elevate your heart rate, burn calories, and boost endurance with our dynamic cardio workouts. From high‑intensity intervals to steady‑state sessions, we’ve got the perfect routine to keep you moving and motivated.</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
            <v-col md="4">
                <v-card>
                    <v-img src="Square1.jpg" cover></v-img>
                    <v-card-title>3.Gym Finder</v-card-title>
                    <v-card-text>Find the perfect gym near you.Discover top‑rated fitness centers, compare amenities, and choose the space that fits your training style.
</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
    
    <!-- Reviews -->
    <v-container>
        <v-row>
            <v-col md="3">
                <v-card color="#cfd0d6">
                    <v-card-text>MacFit is the best gym ever! Loved the experience</v-card-text>
                        <v-rating :length="5" :size="32" :model-value="3" active-color="primary" >
                        </v-rating>
                </v-card>
            </v-col>

            <v-col md="3">
                <v-card color="#cfd0d6">
                    <v-card-text>Had an average experience but all on all, good gym.</v-card-text>
                        <v-rating :length="5" :size="32" :model-value="3" active-color="primary" >
                        </v-rating>
                </v-card>
            </v-col>

            <v-col md="3">
                <v-card color="#cfd0d6">
                    <v-card-text>I had a horrid experience at MacFit. Rude Personnel. #neveragain </v-card-text>
                        <v-rating :length="5" :size="32" :model-value="1" active-color="primary" >
                        </v-rating>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

  <!--Contact Us-->
<v-container style="background-color:#CFD0D6" max-width="100%">
    <v-row class="align-center">
        <div class="text-title-large text-medium-emphasis mb-8" > Get In Touch</div>
        <div class="text-title-large text-medium-emphasis mb-8" > Phone: 0703 034 000. </div>
        <div class="text-title-large text-medium-emphasis mb-8" > Email: macfit@gyms.com.</div>
        <div class="text-title-large text-medium-emphasis mb-8" > Opening Hours</div>
        <div class="text-title-large text-medium-emphasis mb-8" > Monday–Friday, 5:00 am – 10:00 pm (EAT).</div>
        <div class="text-title-large text-medium-emphasis mb-8" > Macfit Gyms, Sangale Road, Nairobi, Kenya.</div>
        <div class="text-title-large text-medium-emphasis mb-8" ></div>
    </v-row>
</v-container>


</template>

    

 