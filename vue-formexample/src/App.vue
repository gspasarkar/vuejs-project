<template>
  <div>
    <component-a/>
    <component-b/>
    <component-c/>
  </div>
</template>

<script>
import ComponentA from './components/ComponentA'
import ComponentB from './components/ComponentB'
import ComponentC from './components/ComponentC'

export default{
  components: {
    ComponentA,
    ComponentB,
    ComponentC
  }
}
</script>
