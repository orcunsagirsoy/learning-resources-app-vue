<template>
  <ul>
      <learning-resource v-for="res in storedResources" 
      :key="res.id" 
      :title="res.title" 
      :description="res.description"
      :link="res.link"
      ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource'


export default {
    components: {
        LearningResource
    },
    data() {
        return {
            storedResources: [
                { 
                    id: 'official-guide', 
                    title: 'official guide', 
                    description: 'the official vue js documentation',
                    link: 'https://vuejs.org'
                },
                { 
                    id: 'google', 
                    title: 'Google', 
                    description: 'Learn to google...',
                    link: 'www.google.com'
                }
            ]
        }
    }
}
</script>

<style>

</style>