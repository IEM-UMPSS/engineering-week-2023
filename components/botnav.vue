<template>
	<v-app-bar location="bottom" density="compact">
		<v-tabs color="teal" centered stacked grow>
					<v-tab to="/" prepend-icon="mdi-home">Home</v-tab>
					<v-tab to="/events" prepend-icon="mdi-calendar-month">Events</v-tab>
					<v-tab to="/committees" prepend-icon="mdi-account">Committees</v-tab>
					<v-tab to="/forum" prepend-icon="mdi-account-group">Forum</v-tab>
					<v-tab to="/announcement" prepend-icon="mdi-bullhorn">Announcement</v-tab>
				</v-tabs>
	</v-app-bar>
</template>