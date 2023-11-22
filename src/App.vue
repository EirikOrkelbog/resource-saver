<template>
  <ul>
    <LearningResource v-for="res in storedResources" :key="res.id" :title="res.title" :description="res.description" :link="res.link"></LearningResource>
  </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource.vue';
export default {
  components: {
    LearningResource
  },
  data() {
    return {
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
  }
}
</script>