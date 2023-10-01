
<template>
  <div id="app">
      {{JSON.stringify(formdata,null,2) }}
      <form name="regForm" @click="submitForm()">
          <div>
            <label for="firstName">First Name:</label>
            <input id="firstName" value="" v-model.trim="formdata.firstName">
          </div>
          <div>
           <label for="lastName">Last Name:</label>
           <input id="lastName" value="" v-model="formdata.lastName">
          </div>
          <div>
            <label for="age">Age:</label>
            <input id="age" value="" v-model.number="formdata.age">
          </div>
          <div>
            <label for="address">Address:</label>
            <textarea id="address" v-model="formdata.address"></textarea>
          </div>
          <div>
            <label for="country">Country:</label>
            <select  name="countries"  v-model="formdata.country">
              <option value="india" select>India</option>
              <option value="usa">USA</option>
              <option value="uk">UK</option>
            </select>
          </div>
          <div>
            <label for="city">City:</label>
            <select  name="cities" v-model="selectedValue" >
              <option v-for="(city,index) of formdata.cities" :key="index" :value="city"  >{{city}}</option>
            </select>
          </div>
      </form>
  </div>
</template>
<script>
/* eslint-disable */
    // add a default exported object export default {}, which is your component object.
    // export default is used to create local registration for Vue component.
    // The first case (export default {...}) is ES2015 syntax for making some object definition available for use.
export default{
  // the registered name of component.
  name: "registration-form",
    // Also, be sure to declare your data properties as functions, otherwise they are not going to be reactive.
    // You'll note that the data property is a function. This is to keep the data values unique for each instance of a component at runtime — the function is invoked separately for each component instance. 
    // If you declared data as just an object, all instances of that component would share the same values. This is a side-effect of the way Vue registers components and something you do not want.
    data() {
      return{
        formdata:{
          firstName: '',
          lastName: '',
          age: null,
          address:'',
          country:'',
          cities:['Pune','Nagpur','Mumbai'],
          selectedValue: 'Mumbai',
        }
      }
    },
    methods: {
      submitForm(){
          this.option.value = selected
      }
    }
}
</script>