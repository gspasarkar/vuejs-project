<template>
<div>
  <p>{{username}}</p><hr>
  <component-a></component-a>
</div>
</template>
<script>
import ComponentA from './components/ComponentA'

export default{
  components: { ComponentA },
  data () {
    return {
      username: 'Raj'
    }
  },
  provide () {
    return {
      username: this.username
    }
  }
}
</script>
