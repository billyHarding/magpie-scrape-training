<script setup>
  import { ref } from 'vue'
  import { useRouter } from 'vue-router'

  const router = useRouter()
    
  const searchTerm = ref('')

  function handleSubmit(event) {
    event.preventDefault();
    router.push({
      path: '/search',
      query: { q: searchTerm.value }
    })
  }
</script>

<template>
  <div class = "container">
    <div class = "header">
      <router-link to="/">
        <img class = "logo" src="https://insight.magpiehq.com/assets/images/magpie-logo-mini.png" />
      </router-link>
      <form @submit="handleSubmit">
        <input type="text" placeholder="Search..." class = "searchbar" v-model="searchTerm">
        </input>
        <input type="submit" value="Search" class="searchbtn"></input>
      </form>
    </div>
    <div class = "content">
      <router-view></router-view>
    </div>
  </div>
</template>

<style scoped>
.container {
  height: 100%;
  display: flex;
  flex-direction: column;
}
.header {
  background-color: #2b3139;
  height: 50px;
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 16px;
}

.header img.logo {
  height: 30px;
}

.header .searchbar {
  height: 30px;
  width: 200px;
  background-color: white;
}

.header .searchbtn {
  height: 30px;
}
.content {
  flex-grow: 1;
  padding: 16px;
}
</style>
