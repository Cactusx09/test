<template>
  <div id="app">
    <tableComponent :tableData="tableData"></tableComponent>
  </div>
</template>

<script>
import tableComponent from './components/table.vue'
export default {
  name: 'app',
  data () {
    return {
      tableData: [
        { id: 1, title: 'Яблоко', weight: 4},
        { id: 2, title: 'Груша', weight: 7},
        { id: 3, title: 'Слива', weight: 1},
      ]
    }
  },
  components: {
    'tableComponent' : tableComponent
  }
}
</script>

<style lang="sass">

</style>
