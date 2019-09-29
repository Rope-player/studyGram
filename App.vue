<template>
  <div id="app">
    <Calendar></Calendar>
    <local-component></local-component>
    <DMPicker></DMPicker>
  </div>
</template>

<script>
  import Calendar from './components/Calendar'

  export default {
    name: 'app',
    components: {Calendar}
  }
</script>
