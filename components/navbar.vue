<template>
	<v-bottom-navigation color="teal" grow>

		<v-btn to="/">
			<v-icon>mdi-home</v-icon>
			Home
		</v-btn>

		<v-btn to="/events">
			<v-icon>mdi-calendar-month</v-icon>
			Events
		</v-btn>

		<v-btn to="/committees" prepend-icon="mdi-account" stacked>
			Committees
		</v-btn>

         <v-btn to="/forum">
			<v-icon>mdi-account-group</v-icon>
			Forum
		</v-btn>

		<v-btn to="/announcement">
			<v-icon>mdi-bullhorn</v-icon>
			Announcement
		</v-btn>

	</v-bottom-navigation>
</template>


<style scoped>
  /* hide certain characters on mobile screens */
  @media only screen and (max-width: 600px) {
    .v-btn__content {
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }
  }
  
  /* show full text on desktop screens */
  @media only screen and (min-width: 601px) {
    .v-btn__content {
      overflow: visible;
      text-overflow: clip;
      white-space: normal;
    }
  }
</style>
