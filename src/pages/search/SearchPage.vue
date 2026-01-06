<script setup>
  import {useRouter} from 'vue-router'
  import StandardSearchPage from './StandardSearchPage.vue'
  import NoResultsSearchPage from './NoResultsSearchPage.vue'
  const props = defineProps({
    query: String
  })
  const router = useRouter()
    
  if (props.query == 'galaxy') {
    router.push('/redirected')
  }

</script>

<template>
  <h1>Search results for: {{ query }}</h1>
  <div class = "search-results">
    <StandardSearchPage v-if="query == 'phone'"></StandardSearchPage>
    <NoResultsSearchPage v-else></NoResultsSearchPage>
  </div>
</template>

<style scoped>
.search-results {
  display: flex;
  flex-wrap: wrap;
}
</style>
