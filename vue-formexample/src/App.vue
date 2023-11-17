<template>
    <component-a>Root App</component-a>
</template>

<script>
import componentA from './components/ComponentA'

export default {
  components: { componentA },
  provide: {
    username: 'John'
  }
}
</script>
