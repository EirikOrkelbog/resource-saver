<template>
  <StoredResources :resources="storedResources"></StoredResources>
</template>

<script>
import StoredResources from './components/learning-resources/StoredResources.vue';
export default {
  components: {
    StoredResources
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

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-family: 'Roboto', sans-serif;
}
</style>