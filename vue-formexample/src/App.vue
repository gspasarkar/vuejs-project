<template>
  <div>
     <p>Search for a film: <input type="text" v-model="filmName"></p>
  </div>
</template>
<script>
export default {
  data () {
    return {
      filmName: 'Jailor'
    }
  },
  watch: {
    filmName: {
      handler (newValue) {
        console.log('Calling API for ' + newValue)
      },
      immediate: true
    }
  }
}
</script>
