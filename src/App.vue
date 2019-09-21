<template>
  <div id="app">
    <Calendar></Calendar>
    <local-component></local-component>
    <DMPicker></DMPicker>
  </div>
</template>

<script>
  import LocalComponent from './components/local-component'
  import Calendar from './components/Calendar'
  import DMPicker from './components/DMPicker'

  export default {
    name: 'app',
    components: {Calendar}
  }
</script>
