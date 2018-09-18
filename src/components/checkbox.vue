<template>
  <div class="g_checkbox">
    <input type="checkbox" id="cb" v-model="checked" v-on:change="change()">
  </div>
</template>
<script>
export default {
  data () {
    return {
      checked: false
    }
  },
  methods: {
    change () {
      console.log(this.checked);
      this.$emit('updateParent', this.checked)
    }
  }
}
</script>
<style lang="scss" scoped>
</style>
