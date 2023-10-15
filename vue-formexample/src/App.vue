<template>
  <div>
    <P>count: {{count}}</P>
    <button @click="count++">Increment</button>
    <button @click="count--">Decrement</button>
  </div>
</template>
<script>
export default{
  data () {
    return {
      count: 0
    }
  },
  watch: {
    count (newValue) {
      if (newValue === 5) {
        alert('Sound is High.')
      }
    }
  }
}
</script>
