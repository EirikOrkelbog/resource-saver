<template>
	<BaseCard>
		<BaseButton @click="setSelectedTab('StoredResources')" :mode="storedResButtonMode">Stored resources</BaseButton>
		<BaseButton @click="setSelectedTab('AddResources')" :mode="addResButtonMode">Add resource</BaseButton>
	</BaseCard>
	<component :is="selectedTab"></component>
</template>

<script>
import StoredResources from './StoredResources.vue';
import AddResources from './AddResource.vue';
export default {
	components: {
		StoredResources,
		AddResources,
	},
	data() {
		return {
			selectedTab: 'StoredResources',
			storedResources: [
				{
					id: 'official guide',
					title: 'Official guide',
					description: 'Official Vue guide',
					link: 'https://vuejs.org/',
				},
				{
					id: 'google',
					title: 'Google',
					description: 'Google website',
					link: 'https://www.google.com/',
				}
			],
		}
	},
	provide() {
		return {
			resources: this.storedResources
		}
	},
	computed: {
		storedResButtonMode() {
			return this.selectedTab === 'StoredResources' ? null : 'flat'; 
		},
		addResButtonMode() {
			return this.selectedTab === 'AddResources' ? null : 'flat'; 
		}
	},
	methods: {
		setSelectedTab(tab) {
			this.selectedTab = tab;
		}
	}
}
</script>