
<template>
  <table>
      <tableCell v-for="key in tableData" :tableRowData="key"></tableCell>
  </table>
</template>

<script>
import tableCell from './tableCell.vue'
export default {
  props: ['tableData'],
  components: {
    'tableCell' : tableCell
  }
}
</script>

<style lang="sass">

</style>
