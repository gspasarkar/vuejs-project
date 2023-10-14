<!--For Notes check Asset folder-->
<template>
  <div id="app">
    Computed {{ isImportant }}<br>
    Method {{ num }}
    <br>
    <input type="text" v-model.lazy="fullName"><br>
    <br>
    <button @click="chkNum()">Save</button>
  </div>
</template>
<script>
export default {
  name: 'computed_property',
  data () {
    return {
      fullName: 'ganesh',
      num: ''
    }
  },
  methods: {
    chkNum () {
      console.log('Method called')
      this.num++
    }
  },
  computed: {
    isImportant () {
      console.log('name computed called')
      if (this.fullName) {
        return this.fullName
      }
    }
  }
}
</script>
