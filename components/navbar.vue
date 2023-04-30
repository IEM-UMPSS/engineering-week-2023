<template>
  <v-bottom-navigation v-model="value" color="teal" style="display:flex; justify-content: space-evenly;  column-gap:  5em;;">
    <router-link to="/">
      <v-btn class="grow" style="text-transform: none; color: initial;">
        <v-icon>mdi-home</v-icon>
        Home
      </v-btn>
    </router-link>
    <router-link to="/events">
      <v-btn class="grow" style="text-transform: none; color: initial;">
        <v-icon>mdi-calendar-month</v-icon>
        Events
      </v-btn>
    </router-link>
    <router-link to="/committee">
      <v-btn class="grow" style="text-transform: none; color: initial;">
        <v-icon>mdi-account-group</v-icon>
        Forum
      </v-btn>
    </router-link>
    <router-link to="/announcement">
      <v-btn class="grow" style="text-transform: none; color: initial;">
        <v-icon>mdi-bullhorn</v-icon>
        News
      </v-btn>
    </router-link>
  </v-bottom-navigation>
</template>

<script>
export default {
  data: () => ({ value: 1 }),
};
</script>
