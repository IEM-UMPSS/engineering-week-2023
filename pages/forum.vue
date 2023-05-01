<template>
	<v-card>
		<v-card-title>Compose a Post</v-card-title>
		<v-divider></v-divider>
		<v-card-text>
			<v-form @submit.prevent="submitPost">
				<v-file-input v-model="postImage" accept="image/*" label="Select an image (optional)"
					hint="Max file size: 2MB"></v-file-input>
				<v-textarea v-model="postText" label="Write your post" required></v-textarea>
				<v-btn type="submit" color="primary">Post</v-btn>
			</v-form>
		</v-card-text>
	</v-card>
</template>

<script setup>
import { ref } from 'vue';

const postImage = ref(null);
const postText = ref('');

function submitPost() {
	// Submit the post to the server
	// using postImage.value and postText.value
}
</script>
