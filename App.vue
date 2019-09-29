<template>
  <v-app id="app">
    <Calendar></Calendar>
  </v-app>
</template>

<script>
  import Calendar from './components/Calendar'

  export default {
    name: 'app',
    components: {Calendar}
  }
</script>
