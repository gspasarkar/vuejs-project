<template>
<div>
  <button @click="filmList.push('Kantara')">Add Film</button>
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
        console.log('Current Films:', newValue)
      },
      deep: true,
      immediate: true
    }
  }
}
</script>
