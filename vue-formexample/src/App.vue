<!--
  ------------------Computed Properies as function example.--------------
Computed properties are like data properties, except they depend on other properties.
Computed properties are written like methods, but they do not accept any input arguments.
Computed properties are updated automatically when a dependency changes, while methods are called on when something happens, like with event handling for example.
Computed properties are used when outputting something that depends on something else.
Computed properties is the third configuration option in the Vue instance that we will learn. The first two configuration options we have already looked at are 'data' and 'methods'.
As with 'data' and 'methods' computed properties also has a reserved name in the Vue instance: 'computed'.
The big advantage with a computed property is that it is dynamic, meaning it changes depending on for example the value of one or more data properties.
 computed properties gives us two important benefits.

    Computed properties are cached, Vue will only re-render the text when one of the names change. This makes the component a lot more performant.
    Because a computed property is a function, we can add complex functionality that we otherwise can’t with just string interpolation.

A common use case would be to calculate and display the total price of items in a shopping cart.

Anything that’s returned from the v-model directive and regular methods aren’t cached. Vue will re-evaluate and re-render it each time an event fires in the rest of the component.

For more complicated logic, you should use computed properties.
-->

<!--This example is to show the difference between the computed properties and methods.-->
<template>
  <div id="app">
    Computed {{isImportant}}<br>
    Method {{num}}
    <br>
    <input type="text" v-model.lazy="fullName" ><br>
    <br>
    <button @click="chkNum()">Save</button>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: 'computed_property',
  data() {
    return {
      fullName: '',
      num:''
    }
  },
  methods: {
    chkNum() {
      console.log("Method called");
      this.num++
    }
  },
  computed: {
    isImportant() {
      console.log("name computed called");
      if(this.fullName) {
        return this.fullName
      }
    }
  }
}
</script>

