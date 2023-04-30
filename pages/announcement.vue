<template>
  <v-card>
    <v-row>
      <v-col cols="2">
        <v-icon size="40">mdi-bell</v-icon>
      </v-col>
      <v-col cols="10">
        <v-card-title>{{ announcementTitle }}</v-card-title>
        <v-card-text>{{ announcementSummary }}</v-card-text>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      announcementTitle: "Important Announcement",
      announcementSummary:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet bibendum ipsum. Mauris posuere, enim vel pulvinar posuere, augue lorem faucibus eros, id dapibus nisl sapien in sem. Nulla sit amet posuere arcu. Sed hendrerit vehicula dolor, at auctor lorem hendrerit id.",
    };
  },
};
</script>
