
<template>
  <!-- <td v-for="cell in tableRowData">{{cell}}</td> -->
  <transition name="fade">
    <tr v-if="!selected">
      <td>{{tableRowData.id}}</td>
      <td><checkbox @updateParent="updateValue"></checkbox></td>
      <td>{{tableRowData.title}}</td>
      <td>{{tableRowData.weight}}</td>
    </tr>
    <tr v-else class="_red">
      <td>-</td>
      <td><checkbox @updateParent="updateValue"></checkbox></td>
      <td>-</td>
      <td>-</td>
    </tr>
  </transition>
</template>

<script>
import checkbox from './checkbox.vue'
export default {
  props: ['tableRowData'],
  data () {
    return {
      selected: false
    }
  },
  methods: {
    updateValue(value) {
      this.selected = value;
    }
  },
  components: {
    'checkbox': checkbox
  }
}
</script>

<style lang="sass">
  #app
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    font-size: 1.3rem;
    font-family: Arial;
  table
    border-collapse: collapse
    width: 520px;
    tr
      border: 3px solid #ccc
      &._red
        position: relative
        z-index: 5
        border-left-color: red
        border-right-color: red
        td
          border-top: 3px solid red
          border-bottom: 3px solid red
      td
        padding: 1vh 5vh

</style>
