<template>
 <div>
   <button @click="isMenuOpen=true">Open Menu</button>
   <component-mainmenu v-show="isMenuOpen" @closeMenu="isMenuOpen=false">Main Menu</component-mainmenu>
 </div>
</template>
<script>
import MainMenu from './components/MainMenu.vue'

export default{
  components: { MainMenu },
  data () {
    return {
      isMenuOpen: false
    }
  }
}
</script>
