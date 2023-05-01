<template>
	<v-carousel cycle show-arrows="hover" progress="success" color="teal">
		<v-carousel-item v-for="(slide, i) in slides" :src="slide.src" :key="i"></v-carousel-item>
	</v-carousel>
</template>

<script setup>
const slides = [
	{
		src: '/slides/1.jpg',
	},
	{
		src: '/slides/2.jpg',
	},
	{
		src: '/slides/3.jpg',
	},
]

</script>
