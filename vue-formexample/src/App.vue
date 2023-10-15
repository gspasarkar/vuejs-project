<template>
  <div>
    <p>Full Name: {{ fullName }}</p>
    <p>First Name: {{ firstName }}</p>
    <p>Last Name: {{ lastName }}</p>
    <input type="text" v-model.lazy.trim="fullName">
    <button @click="changeName">Update</button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      firstName: 'Kapil',
      lastName: 'Jagtap'
    }
  },
  methods: {
    changeName () {
      this.fullName = 'Vijay Nagle'
    }
  },
  computed: {
    fullName: {
      get () {
        return this.firstName + ' ' + this.lastName
      },
      set (name) {
        console.log(name)
        const names = name.split(' ')
        this.firstName = names[0]
        this.lastName = names[1]
      }
    }
  }
}
</script>
