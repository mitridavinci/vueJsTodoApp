<script>
import Contains from "./components/Contains.vue"
export default {
  name: 'App',
  components: {
    'contains': Contains
  }
}
</script>

<template>
      <div id="app">
        <contains></contains>
      </div>
</template>

<style scoped>
  body{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
