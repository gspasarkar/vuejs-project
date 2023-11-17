<template>
 <div>
  <button @click="$emit('closeMenu')">Close Me</button>
 </div>
</template>
<script>
export default{
  emits: ['closeMenu']
}
</script>
