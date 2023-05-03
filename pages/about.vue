<template>
	<v-container>
		<v-row>
			<v-col>
				<v-card>
					<v-card-title class="text-h4">About</v-card-title>
					<v-card-text>
						Engineering Week is an annual event that celebrates the field of engineering and its contributions to society.
						Join us for a week of exciting events and activities that showcase the innovative and creative side of
						engineering!
					</v-card-text>
				</v-card>
			</v-col>
		</v-row>
		<v-row>
			<v-col cols="12">
				<h1>Our Team</h1>
			</v-col>
			<v-col v-for="(member, index) in members" :key="index" cols="6" sm="4" lg="3" class="text-center">
				<v-avatar size="80">
					<v-img :src="member.avatar" />
				</v-avatar>

				<h3>{{ member.name }}</h3>
				<v-chip color="teal">{{ member.jobTitle }}</v-chip>
			</v-col>
		</v-row>
	</v-container>
</template>

<script setup>
import { ref } from 'vue';

const members = ref([
	{
		name: "John Doe",
		jobTitle: "Chairperson",
		avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
	},
	{
		name: "Jane Smith",
		jobTitle: "Vice Chairperson",
		avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
	},
	{
		name: "Bob Johnson",
		jobTitle: "Secretary",
		avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
	},
	{
		name: "Sarah Lee",
		jobTitle: "Treasurer",
		avatar: "https://cdn.vuetifyjs.com/images/lists/4.jpg",
	},
	{
		name: "John Doe",
		jobTitle: "Chairperson",
		avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
	},
	{
		name: "Jane Smith",
		jobTitle: "Vice Chairperson",
		avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
	},
	{
		name: "Bob Johnson",
		jobTitle: "Secretary",
		avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
	},
	{
		name: "Sarah Lee",
		jobTitle: "Treasurer",
		avatar: "https://cdn.vuetifyjs.com/images/lists/4.jpg",
	},
	{
		name: "John Doe",
		jobTitle: "Chairperson",
		avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
	},
	{
		name: "Jane Smith",
		jobTitle: "Vice Chairperson",
		avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
	},
	{
		name: "Bob Johnson",
		jobTitle: "Secretary",
		avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
	},
	{
		name: "Sarah Lee",
		jobTitle: "Treasurer",
		avatar: "https://cdn.vuetifyjs.com/images/lists/4.jpg",
	},
]);
</script>
