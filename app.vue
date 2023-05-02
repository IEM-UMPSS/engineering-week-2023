<template>
	<v-card>
		<v-app>
			<v-app-bar density="compact" scroll-behavior="hide">
				<v-toolbar-title>Engineering Week</v-toolbar-title>
				<template v-slot:append>
					<v-btn @click="toggleTheme"
						:icon="theme.global.current.value.dark ? 'mdi-weather-night' : 'mdi-weather-sunny'"></v-btn>
				</template>
			</v-app-bar>

			<v-main>
				<v-container fluid>
					<RouterView />
					<Footer />
				</v-container>
			</v-main>

			<botnav />
		</v-app>
	</v-card>
</template>

<script setup>
import { RouterView } from 'vue-router'
import { useTheme } from 'vuetify'
import Footer from './components/footer.vue'
import botnav from './components/botnav.vue'

const toggleTheme = () => theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
const theme = useTheme()

</script>
