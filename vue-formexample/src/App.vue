/* eslint-disable */
<template>
<div>
  <button @click="filmList.push('Titanic')">Add Film</button>
</div>
</template>
<script>
export default {
  data () {
    return {
      filmList: ['Jailor', 'Jawaan']
    }
  },
  watch: {
    filmList: {
      handler (newValue) {
        console.log('Movie Title', newValue)
      },
      deep: true
    }
  }
}
</script>
