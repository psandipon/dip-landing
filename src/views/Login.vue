<template>
  <div>
    <v-card
      tile
      :height="$vuetify.breakpoint.height"
      :width="$vuetify.breakpoint.width"
      color="#717672"
      class="justify-center align-center d-flex"
      :class="ifPhone ? 'pa-0' : 'py-16'"
    >
      <v-container>
        <v-row no-gutters>
          <v-col no-gutters cols="12" md="6">
            <v-card
              color="white"
              :height="getHeight"
              class="infoCard d-flex flex-column"
              :class="ifPhone ? 'pa-0' : ' my-16 ml-16'"
              flat
              tile
              v-if="!ifPhone"
            >
              <v-img
                :src="require('@/assets/logo.png')"
                contain
                :aspect-ratio="ifPhone ? '10' : '4'"
                :class="ifPhone ? 'ma-16 pa-16' : 'mt-16'"
              />
              <v-card :class="ifPhone ? 'mt-n16 ' : 'pa-5 ma-16 rounded-lg'">
                <span>
                  The Data Integration Platform (DIP) supports clinical
                  research. It serves to provide various applications for
                  medical research purposes. The platform provides a
                  comprehensive versioned data storage, as well as rights and
                  user management. Central data storage enables reuse for other
                  research purposes.
                </span>
              </v-card>
            </v-card>
            <v-card color="white" flat tile class="pa-10" v-else>
              <v-img
                :src="require('@/assets/logo.png')"
                contain
                :aspect-ratio="ifPhone ? '10' : '4'"
                :class="ifPhone ? 'ma-16 pa-16' : 'mt-16'"
              />
              <v-card
                :class="ifPhone ? 'mt-n16 ' : 'pa-5 ma-16 rounded-lg'"
                flat
              >
                <span>
                  The Data Integration Platform (DIP) supports clinical
                  research. It serves to provide various applications for
                  medical research purposes. The platform provides a
                  comprehensive versioned data storage, as well as rights and
                  user management. Central data storage enables reuse for other
                  research purposes.
                </span>
              </v-card>
            </v-card>
          </v-col>
          <v-col no-gutters cols="12" md="6">
            <v-card
              color="white"
              :height="$vuetify.breakpoint.height / 2"
              :class="ifPhone ? 'pa-16 ' : ' my-16 mr-16'"
              class="d-flex flex-column justify-center align-center"
              flat
              tile
              v-if="!ifPhone"
            >
              <span class="text-h5">
                DATA INTEGRATION PLATFORM
              </span>
              <span class="my-10 text-h5">
                Welcome to DIP
              </span>
              <span>
                <v-text-field
                  color="#80BA27"
                  label="Email"
                  :width="$vuetify.breakpoint.width"
                ></v-text-field>
              </span>
              <span>
                <v-text-field
                  color="#80BA27"
                  label="Email"
                  :width="$vuetify.breakpoint.width"
                  type="password"
                >
                </v-text-field>
              </span>
              <v-text-feild label="Email"> </v-text-feild>
              <v-text-feild label="Password" type="password"> </v-text-feild>
              <br />
              <br />
              <span color="">
                Fongot your password ?
              </span>
              <v-btn
                x-large
                class="rounded-lg mt-16"
                large
                dark
                depressed
                color="#80BA28"
                @click="goto('/login')"
              >
                LOGIN
              </v-btn>
            </v-card>
            <!-- below is the ui for phone  -->
            <v-card color="white" flat tile class="pa-10" v-else>
              <span class="text-h5">
                DATA INTEGRATION PLATFORM
              </span>
              <span class="my-10 text-h5">
                Welcome to DIP
              </span>
              <span>
                <v-text-field
                  color="#80BA27"
                  label="Email"
                  :width="$vuetify.breakpoint.width"
                ></v-text-field>
              </span>
              <span>
                <v-text-field
                  color="#80BA27"
                  label="Email"
                  :width="$vuetify.breakpoint.width"
                  type="password"
                >
                </v-text-field>
              </span>
              <v-text-feild label="Email"> </v-text-feild>
              <v-text-feild label="Password" type="password"> </v-text-feild>
              <br />
              <br />
              <span color="">
                Fongot your password ?
              </span>
              <v-btn
                x-large
                class="rounded-lg mt-16"
                large
                dark
                depressed
                color="#80BA28"
                @click="goto('/login')"
              >
                LOGIN
              </v-btn>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "Home",
  computed: {
    ifPhone() {
      return this.$vuetify.breakpoint.mobile;
    },
    getHeight() {
      if (this.ifPhone) {
        return (
          this.$vuetify.breakpoint.height + this.$vuetify.breakpoint.height / 2
        );
      } else {
        return this.$vuetify.breakpoint.height / 2;
      }
    },
  },
};
</script>

<style scoped>
.infoCard {
  background: linear-gradient(180deg, #80ba28 0%, #50708d 100%);
}
</style>
