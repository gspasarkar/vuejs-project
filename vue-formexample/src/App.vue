<template>
  <div>
    <p>Count:{{ count }}</p>
    <button @click=count++>Increment</button>
    <button @click=count-->Decrement</button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      count: 0
    }
  },
  watch: {
    count (newValue, oldValue) {
      if (newValue > oldValue && oldValue === 5) {
        alert('You are at peak sound, this is danger for you.')
      }
    }
  }
}
</script>
