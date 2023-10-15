<template>
  <div>
    <p>Enter Film Title:<input type="text" v-model.lazy="film.title"></p>
    <p>Film Title:{{ film.title }}</p>
  </div>
</template>
<script>
export default {
  data () {
    return {
      film: {
        title: ''
      }
    }
  },
  watch: {
    film: {
      handler (newValue) {
        console.log('Hello')
        console.log('Film: ' + newValue.title)
      },
      deep: true
    }
  }
}
</script>
