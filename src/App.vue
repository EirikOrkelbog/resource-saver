<template>
  <ul>
    <li v-for="res in storedResources" :key="res.id">
      <div>
        <header>
          <h3>{{ res.title }}</h3>
          <button>Delete</button>
        </header>
      </div>
      <p>{{ res.description }}</p>
      <nav>
        <a :href="res.link">See resource</a>
      </nav>
    </li>
  </ul>
</template>

<script>
export default {
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