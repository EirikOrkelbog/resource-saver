<template>
	<ul>
		<LearningResource v-for="res in resources" :key="res.id" :title="res.title" :description="res.description"
			:link="res.link"></LearningResource>
	</ul>
</template>

<script>
import LearningResource from './LearningResource.vue';
	export default {
		inject: ['resources'],
		components: {
			LearningResource
		}
	}
</script>

<style scoped>
ul {
	list-style: none;
	margin: auto;
	max-width: 40rem;
}
</style>