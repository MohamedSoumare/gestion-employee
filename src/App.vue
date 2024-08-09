<template>
  <div id="app">
    <ListEmployee />
  </div>
</template>

<script>
import ListEmployee from './components/ListEmployee.vue';

export default {
  name: 'App',
  components: {
    ListEmployee,
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

h1 {
  font-size: 24px;
  color: #121212;
  margin-bottom: 20px;
}
</style>
