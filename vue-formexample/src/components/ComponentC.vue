<template>
<div>
  <p>Component C</p>
  <p>{{username}}</p>
</div>
</template>
<script>
export default {
  name: 'ComponentC',
  inject: ['username']
}
</script>
