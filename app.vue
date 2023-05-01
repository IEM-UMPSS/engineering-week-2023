<template>
	<v-card>
		<v-app>
			<v-app-bar>
				<v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
				<v-toolbar-title>Engineering Week</v-toolbar-title>
				<template v-slot:append>
					<v-btn @click="toggleTheme"
						:icon="theme.global.current.value.dark ? 'mdi-weather-night' : 'mdi-weather-sunny'"></v-btn>
				</template>
			</v-app-bar>

			<v-navigation-drawer v-model="drawer" temporary>
				<v-list color="teal">
					<v-list-item to="/" prepend-icon="mdi-home">Home</v-list-item>
					<v-list-item to="/events" prepend-icon="mdi-calendar-month">Events</v-list-item>
					<v-list-item to="/committees" prepend-icon="mdi-account">Committees</v-list-item>
					<v-list-item to="/forum" prepend-icon="mdi-account-group">Forum</v-list-item>
					<v-list-item to="/announcement" prepend-icon="mdi-bullhorn">Announcement</v-list-item>
				</v-list>
			</v-navigation-drawer>

			<v-main>
				<v-container fluid>
					<RouterView />
				</v-container>
			</v-main>
		</v-app>
	</v-card>
</template>

<script setup>
import { RouterView } from 'vue-router'
import { useTheme } from 'vuetify'
import { ref, watch } from 'vue'

const drawer = ref(false)
const group = ref(null)

const toggleTheme = () => theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
const theme = useTheme()

watch(group, () => {
	drawer.value = false
})

</script>
