<template>
  <v-app>
    <Navbar />
    <router-view />
  </v-app>
</template>
<script>
import Navbar from './components/navbar.vue'

export default {
  components: {
    Navbar,
  }
}
</script>