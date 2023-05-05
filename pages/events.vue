<template>
	<v-container>
		<v-row>
			<v-col cols="12">
				<h1>Events</h1>
			</v-col>

			<v-col cols="12" class="hidden-sm-and-down">
				<v-timeline line-inset="12">
					<v-timeline-item v-for="(event, i) in events" :key="i" width="100%">
						<template v-slot:opposite>
							{{ event.date }}
						</template>
						<v-card>
							<v-img class="align-end text-white" height="200" :src="event.poster" cover>
								<v-card-title>{{ event.title }}</v-card-title>
							</v-img>

							<v-card-subtitle class="pt-4">
								<v-icon icon="mdi-map-marker"></v-icon>
								{{ event.venue }}
							</v-card-subtitle>

							<v-card-text>
								<div>Organizer: {{ event.organizer }}</div>
							</v-card-text>

							<v-card-actions>
								<v-btn color="teal">
									Join
								</v-btn>

								<v-btn color="teal">
									Learn More
								</v-btn>
							</v-card-actions>
						</v-card>
					</v-timeline-item>
				</v-timeline>
			</v-col>

			<v-col cols="12" v-for="(event, i) in events" :key="i" class="hidden-md-and-up">
				<v-card>
					<v-img class="align-end text-white" height="200" :src="event.poster" cover>
						<v-card-title>{{ event.title }}</v-card-title>
					</v-img>

					<v-card-subtitle class="pt-4">
						<v-icon icon="mdi-map-marker"></v-icon>
						{{ event.venue }}
					</v-card-subtitle>

					<v-card-text>
						<div>Date: {{ event.date }}</div>
						<div>Organizer: {{ event.organizer }}</div>
					</v-card-text>

					<v-card-actions>
						<v-btn color="teal">
							Join
						</v-btn>

						<v-btn color="teal">
							Learn More
						</v-btn>
					</v-card-actions>
				</v-card>
			</v-col>
		</v-row>
	</v-container>
</template>

<script setup>
const events = [
	{
		title: 'Engineering Fair',
		date: 'Monday, February 20th',
		venue: 'Engineering Building',
		poster: 'https://via.placeholder.com/300x200?text=Engineering+Fair',
		organizer: 'IEM Pahang',
	},
	{
		title: 'Industry Networking Night',
		date: 'Tuesday, February 21st',
		venue: 'Student Center',
		poster: 'https://via.placeholder.com/300x200?text=Industry+Networking+Night',
		organizer: 'Dancing Club',
	},
	{
		title: 'Hackathon',
		date: 'Wednesday, February 22nd',
		venue: 'Computer Science Lab',
		poster: 'https://via.placeholder.com/300x200?text=Hackathon',
		organizer: 'ADAB',
	},
	{
		title: 'Keynote Speaker',
		date: 'Thursday, February 23rd',
		venue: 'Auditorium',
		poster: 'https://via.placeholder.com/300x200?text=Keynote+Speaker',
		organizer: 'JHEPA',
	},
	{
		title: 'Robotics Competition',
		date: 'Friday, February 24th',
		venue: 'Gymnasium',
		poster: 'https://via.placeholder.com/300x200?text=Robotics+Competition',
		organizer: 'FKOM',
	},
	{
		title: 'Engineering Fair',
		date: 'Monday, February 20th',
		venue: 'Engineering Building',
		poster: 'https://via.placeholder.com/300x200?text=Engineering+Fair',
		organizer: 'FTKEE',
	},
	{
		title: 'Industry Networking Night',
		date: 'Tuesday, February 21st',
		venue: 'Student Center',
		poster: 'https://via.placeholder.com/300x200?text=Industry+Networking+Night',
		organizer: 'Huawei Malaysia',
	},
	{
		title: 'Hackathon',
		date: 'Wednesday, February 22nd',
		venue: 'Computer Science Lab',
		poster: 'https://via.placeholder.com/300x200?text=Hackathon',
		organizer: 'Microsoft Malaysia',
	},
	{
		title: 'Keynote Speaker',
		date: 'Thursday, February 23rd',
		venue: 'Auditorium',
		poster: 'https://via.placeholder.com/300x200?text=Keynote+Speaker',
		organizer: 'UTM Johor Bahru',
	},
	{
		title: 'Robotics Competition',
		date: 'Friday, February 24th',
		venue: 'Gymnasium',
		poster: 'https://via.placeholder.com/300x200?text=Robotics+Competition',
		organizer: 'Universiti Sains Malaysia',
	},
];
</script>
