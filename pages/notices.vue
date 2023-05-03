<template>
	<v-container>
		<v-row>
			<v-col cols="12">
				<h1>Notices</h1>
			</v-col>

			<v-col v-for="(notice, i) in notices" :key="i" cols="12">
				<v-card prepend-icon="mdi-bell">
					<template v-slot:title>
						{{ notice.title }}
					</template>
					<v-card-text>{{ notice.content }}</v-card-text>
				</v-card>
			</v-col>
		</v-row>
	</v-container>
</template>

<script setup>
const notices = [
	{
		title: "Important Announcement",
		content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet bibendum ipsum. Mauris posuere, enim vel pulvinar posuere, augue lorem faucibus eros, id dapibus nisl sapien in sem. Nulla sit amet posuere arcu. Sed hendrerit vehicula dolor, at auctor lorem hendrerit id."
	},
	{
		title: "Important Announcement",
		content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet bibendum ipsum. Mauris posuere, enim vel pulvinar posuere, augue lorem faucibus eros, id dapibus nisl sapien in sem. Nulla sit amet posuere arcu. Sed hendrerit vehicula dolor, at auctor lorem hendrerit id."
	},
	{
		title: "Important Announcement",
		content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet bibendum ipsum. Mauris posuere, enim vel pulvinar posuere, augue lorem faucibus eros, id dapibus nisl sapien in sem. Nulla sit amet posuere arcu. Sed hendrerit vehicula dolor, at auctor lorem hendrerit id."
	},
	{
		title: "Important Announcement",
		content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet bibendum ipsum. Mauris posuere, enim vel pulvinar posuere, augue lorem faucibus eros, id dapibus nisl sapien in sem. Nulla sit amet posuere arcu. Sed hendrerit vehicula dolor, at auctor lorem hendrerit id."
	},
]
</script>
