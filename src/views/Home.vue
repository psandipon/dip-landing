<template>
  <div>
    <!-- :height="$vuetify.breakpoint.height - 300" -->
    <v-img
      :src="require('@/assets/hero.png')"
      :aspect-ratio="ifPhone ? '1' : '3.5'"
    >
      <v-container>
        <div class="" :class="ifPhone ? 'ma-10 mt-16' : 'my-16 py-16'">
          <span class="white--text" :class="ifPhone ? 'text-h4' : ' heroText'">
            DATA <br />
            INTEGRATION<br />
            PLATFORM
          </span>
          <br />
          <br />
          <v-btn
            large
            dark
            depressed
            class="rounded-lg btnStyle"
            @click="goto('/login')"
          >
            <span class="px-5 font-weight-bold text-h5 ">LOGIN</span>
          </v-btn>
        </div>
      </v-container>
    </v-img>
    <v-row class="justify-center align-center d-flex">
      <span class="ma-16 text-h4">
        In coorperation with
      </span>
    </v-row>
    <v-row>
      <!-- :aspect-ratio="ifPhone ? '1' : '3'" -->
      <v-col cols="12" md="4">
        <v-img :src="require('@/assets/thm.png')" :aspect-ratio="5" contain />
      </v-col>
      <v-col cols="12" md="4">
        <v-img :src="require('@/assets/ukgm.png')" :aspect-ratio="5" contain />
      </v-col>
      <v-col cols="12" md="4">
        <v-img :src="require('@/assets/jlu.png')" :aspect-ratio="5" contain />
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Home",
  computed: {
    ifPhone() {
      return this.$vuetify.breakpoint.mobile;
    },
  },
  methods: {
    goto(link) {
      // console.log("link:", link);
      this.$router.push(link);
    },
  },
};
</script>

<style scoped>
.heroText {
  font-size: 80px;
  line-height: 103px;
  letter-spacing: 0.23em;
}
.btnStyle {
  background: linear-gradient(
    90deg,
    rgba(255, 255, 255, 0) 0%,
    rgba(185, 228, 240, 0.229167) 0.01%,
    #7be969 113.75%
  );
  border-radius: 8px;
  letter-spacing: 0.15em;
}
</style>
