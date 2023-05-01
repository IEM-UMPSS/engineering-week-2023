<template>
	<div>
		<h1>Committee Members</h1>
		<div class="d-flex justify-center">
			<div>
				<div v-for="(member, index) in members" :key="index">
					<v-avatar size="80">
						<v-img :src="member.avatar" />
					</v-avatar>
					<h3>{{ member.name }}</h3>
					<p>{{ member.jobTitle }}</p>
				</div>
			</div>
		</div>
	</div>
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
]);
</script>
