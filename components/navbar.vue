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

		<v-btn to="/committee">
			<v-icon>mdi-account-group</v-icon>
			Forum
		</v-btn>

		<v-btn to="/announcement">
			<v-icon>mdi-bullhorn</v-icon>
			News
		</v-btn>

	</v-bottom-navigation>
</template>
