<template>
  <v-app>
    <v-content>
      <SquidKing />
    </v-content>
  </v-app>
</template>

<script>
import SquidKing from './components/SquidKing.vue'

export default {
  name: 'App',

  components: {
    SquidKing
  },

  data: () => ({
    //
  }),
};
</script>

<style>
  @font-face {
      font-family: 'GongGothicMedium';
      src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_20-10@1.0/GongGothicMedium.woff') format('woff');
      font-weight: normal;
      font-style: normal;
  }
  * {
      font-family: 'GongGothicMedium';
      font-weight: 300;
  }
</style>
