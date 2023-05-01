<template>
	<v-card>
		<v-card-title>Events</v-card-title>
		<v-row>
			<v-col v-for="event in events" :key="event.id" cols="12" md="6">
				<v-card>
					<v-img :src="event.poster" height="200"></v-img>
					<v-card-title>{{ event.title }}</v-card-title>
					<v-card-subtitle>{{ event.date }}</v-card-subtitle>
					<v-card-subtitle>{{ event.location }}</v-card-subtitle>
				</v-card>
			</v-col>
		</v-row>
	</v-card>
</template>

<script setup>
const events = [
	{
		id: 1,
		title: 'Engineering Fair',
		date: 'Monday, February 20th',
		location: 'Engineering Building',
		poster: 'https://via.placeholder.com/300x200?text=Engineering+Fair'
	},
	{
		id: 2,
		title: 'Industry Networking Night',
		date: 'Tuesday, February 21st',
		location: 'Student Center',
		poster: 'https://via.placeholder.com/300x200?text=Industry+Networking+Night'
	},
	{
		id: 3,
		title: 'Hackathon',
		date: 'Wednesday, February 22nd',
		location: 'Computer Science Lab',
		poster: 'https://via.placeholder.com/300x200?text=Hackathon'
	},
	{
		id: 4,
		title: 'Keynote Speaker',
		date: 'Thursday, February 23rd',
		location: 'Auditorium',
		poster: 'https://via.placeholder.com/300x200?text=Keynote+Speaker'
	},
	{
		id: 5,
		title: 'Robotics Competition',
		date: 'Friday, February 24th',
		location: 'Gymnasium',
		poster: 'https://via.placeholder.com/300x200?text=Robotics+Competition'
	}
];
</script>
