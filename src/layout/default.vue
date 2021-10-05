<template>
  <div>
    <v-app-bar app dark color="#56595C" flat>
      <div class="d-flex align-center">
        <v-img
          alt="Dip Logo"
          class="shrink mr-2"
          contain
          :src="require('@/assets/dip.png')"
          transition="scale-transition"
          width="100"
          @click="goto('/')"
        />
      </div>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </div>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
