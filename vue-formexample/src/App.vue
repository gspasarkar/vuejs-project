<template>
<dynamic-prop v-bind:fullName="fullName"></dynamic-prop>
</template>
<script>
import DynamicProp from './components/DynamicProp'
export default{
  components: {DynamicProp},
  data () {
    return {
      firstName: 'Ganesh',
      lastName: 'Pasarkar'
    }
  },
  computed: {
    fullName () {
      return this.firstName + ' ' + this.lastName
    }
  }
}
</script>
