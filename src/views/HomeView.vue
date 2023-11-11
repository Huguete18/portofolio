<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'm Sergi Huguet</h1>
              <span class="text-grey">Web Designer & Developer</span><br />
              <v-btn tile dark class="text-red mt-8" variant="outlined">Contact me</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="position: absolute; z-index: 9999; bottom: 0; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999;" class="mt-16">
              <v-img src="i1.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about" >
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="i2.png" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About Me</h5>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="red"> //Debería de ir después del color="yellow" un label="track-color"
                </v-slider>
              </div>
              <h4 class="mt-n4">I Am a Creative Web Design</h4>
              <h4>And Developer</h4>
              <p class="text-grey">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi praesentium, sit eius quo molestiae laudantium minus qui soluta odio inventore tempora delectus autem, cum illo repellat ea quis assumenda in!</p>
              <br />
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis enim minima aut odit repellendus quo perspiciatis, quod doloribus non, nihil, ex vero. Consectetur repudiandae explicabo neque? Rem perferendis ex temporibus?
              </p>
              <v-btn tile dark color="red" class="mt-4">
                Download Resume
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What we Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="red">//Debería de ir después del color="yellow" un label="track-color"
          </v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portofolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="#fb7e7e" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet <br /> consectetur adipisicing <br /> consectetur adipisicing
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-mobile-alt" color="#fb7e7e" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet <br /> consectetur adipisicing <br /> consectetur adipisicing
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-camera" color="#fb7e7e" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Photography</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet <br /> consectetur adipisicing <br /> consectetur adipisicing
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#fb7e7e" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Fron Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">Illustration</v-btn>
        </div>
      </v-col>
    </v-container>
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';
import NavBar from '@/components/NavBar.vue';

export default defineComponent({
  name: 'HomeView',
  setup(){
    return {
      slider2: 50,

      items: [
        {
          img: "i3.jpg",
        },
        {
          img: "i4.jpg",
        },
        {
          img: "i5.jpg",
        },
        {
          img: "i6.jpg",
        },
        {
          img: "i9.jpg",
        },
        {
          img: "i8.jpg",
        },
      ],
    }
  },

  components: {
    NavBar
  },
});
</script>
<style scoped>
  .v-container {
    padding: 16px 0;
  }
  .head {
    position: relative;
    text-align: center;
    padding: 12px;
    margin-bottom: 6px;
    height: 400px;
    width: 100%;
    color: white;
  }
  .head:before {
    content: "";
    position :absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 50%;
    background: black;
    transform: skew(0deg, 5deg);
  }
  .head:after {
    content: "";
    position :absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 50%;
    background: black;
    transform: skew(0deg, -5deg);
  }
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>
