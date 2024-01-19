<template>
  <Navbar />
  <v-main>
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-row>
            <v-col cols="12" sm="6">
              <h1 class="title1">
                <span class="title1__span">Travel</span> with us <br />
                <span class="title1__span">Enjoy</span> your life
              </h1>
              <p class="par1">
                Lorem ipsum dolor sit amet consectetur.<br />
                Quisquam voluptatum, quibusdam, voluptate,<br />
                exercitationem quos doloribus quas.
              </p>
              <v-btn
                class="text-noe mt-8 bt1"
                color="indigo-lighten-1"
                size="x-large"
                variant="flat"
                rounded="0"
              >
                Get Explore
              </v-btn>
              <v-btn
                class="text-none ml-2 text-indigo-lighten-1 mt-8"
                size="x-large"
                variant="flat"
                rounded="0"
              >
                Read More
              </v-btn>
            </v-col>
            <v-col cols="12" sm="6">
              <v-img class="img1" src="/3.jpg"></v-img>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="12">
          <v-card flat>
          <v-tabs v-model="tab" color="indigo-lighten-1" align-tabs="center">
          <v-tab :value="1">
          <v-icon class="mr-2">mdi mdi-bed</v-icon>Hotel
          </v-tab>
          <v-tab :value="2">
          <v-icon class="mr-2">mdi mdi-airplane-takeoff</v-icon>Flight
          </v-tab>
          <v-tab :value="3">
          <v-icon class="mr-2">mdi mdi-car</v-icon>Car
          </v-tab>
          <v-tab :value="4">
          <v-icon class="mr-2">mdi mdi-ferry</v-icon>Ship
          </v-tab>
        </v-tabs>
        <v-window v-model="tab">
        <v-window-item v-for="n in 4" :key="n" :value="n">
          <v-container fluid>
            <v-row>
              <v-col cols="12" sm="2">
                <div class="text-subtile-1 text-medium-emphasis">Your Destination</div>
                <v-select density="compact" placeholder="Destination"  :items="[
                            'Paris',
                            'Amsterdam',
                            'New York',
                            'London',
                            'California',
                            'Dubai',
                            'Singapore',
                          ]"
                          variant="outlined"></v-select>
              </v-col>
              <v-col cols="12" sm="2">
                <div class="text-subtile-1 text-medium-emphasis">Check in</div>
                <v-text-field density="compact" placeholder="Date" type="date" variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="2">
                <div class="text-subtile-1 text-medium-emphasis">Check out</div>
                <v-text-field density="compact" placeholder="Date" type="date" variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="2">
                <div class="text-subtile-1 text-medium-emphasis">Child</div>
                <v-select density="compact" placeholder="Child"  :items="[
                            '1',
                            '2',
                            '3',
                            '4',
                            '5',
                            '6',
                          ]"
                          variant="outlined"></v-select>
              </v-col>
              <v-col cols="12" sm="2">
                <div class="text-subtile-1 text-medium-emphasis">Adult</div>
                <v-select density="compact" placeholder="Adult"  :items="[
                            '1',
                            '2',
                            '3',
                            '4',
                            '5',
                            '6',
                          ]"
                          variant="outlined"></v-select>
              </v-col>
              <v-col cols="12" sm="2">
                <v-btn class="text-none mt-5" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                  Book Now
                </v-btn>
              </v-col>
            </v-row>
          </v-container>
        </v-window-item>
      </v-window>
        </v-card>
        </v-col>
        <v-col cols="12" sm="12">
          <h4 class="text-center text-indigo-lighten-1">Featured Tours</h4>
          <h1 class="text-center">Beautiful Places Around The World</h1>
          <v-row justify="center">
            <v-col cols="12" sm="10">
              <v-row>
                <v-col cols="12" sm="4">
                  <v-hover v-slot="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover':isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%"></v-img>
                      <div class="d-flex flex-row-reverse">
                        <v-btn class="text-none" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                          3 Packages
                        </v-btn>
                      </div>
                    </v-card>
                  </v-hover>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
  <Footer />
</template>

<script setup>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
</script>

<script>
export default {
  data: () => ({
    tab: null,
    model: null,
    icons: ["mdi-rewind", "mdi-play", "mdi-fast-forward"],
    transparent: "rgba(255, 255, 255, 0)",
    rating: 4.5,
  })
};
</script>

<style scoped>
.title1 {
  color: #1f3347;
  font-size: 45px;
  font-style: bold;
  margin-left: 100px;
  margin-top: 70px;
}
.par1 {
  color: #aaa1b4;
  margin-left: 100px;
}
.bt1 {
  margin-left: 100px;
}
.img1 {
  width: 1000px !important;
  height: 1000px !important;
  z-index: 1;
  margin-top: -200px;
}
</style>
