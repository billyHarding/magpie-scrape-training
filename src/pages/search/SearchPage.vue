<script setup>
  import {useRouter} from 'vue-router'
  import BasicSearchPage from './BasicSearchPage.vue'
  import DetailedSearchPage from './DetailedSearchPage.vue'
  import NoResultsSearchPage from './NoResultsSearchPage.vue'
  const props = defineProps({
    query: String
  })
  const router = useRouter()
</script>

<template>
  <h1>Search results for: {{ query }}</h1>
  <div class = "search-results">
    <NoResultsSearchPage v-if="query == 'ifone'"></NoResultsSearchPage>
    <BasicSearchPage v-else-if="query == 'new phone'"></BasicSearchPage>
    <DetailedSearchPage v-else></DetailedSearchPage>
  </div>
</template>

<style scoped>
.search-results {
  display: flex;
  flex-wrap: wrap;
}
</style>
