<template>
  <section class="container">
    {{ mydata }} <h1>{{ title }}</h1>
    <p id="demo"/>
  
    <!--<form name="myForm" action=""  method="post">-->
    <!--<input type="text" id="Name" value="">-->
     
     <label for="name"/>Name
       &nbsp;
      <input type="text"
        v-model="name"
        />
      <br>
     <label for="email"/>Email
     &nbsp;
      <input
        v-model="email"
        type="text" >
      <br>
      <input
        type="button"
        value="Submit"
        @click="validateForm">
        <!--</form>-->
  <!--<nuxt-link to="/">Home page</nuxt-link>-->
  </section>
</template>

<script>
export default {
  data() {
    return {
      mydata: 'hello',
      title: 'iftekhar',
      name:'',
      email:''
 
    }
  },

  beforecreated: function() {
    console.log('this is beforecreated ')
  },
  created: function() {
    // `this` points to the vm instance
    console.log('this is created ')
  },

  beforeMount: function() {
    // `this` points to the vm instance
    console.log('this is beforeMount ')
  },
  mounted: function() {
    // `this` points to the vm instance
    console.log('this is mounted ')
  },
  methods: {
    validateForm: function(event) {
      console.log('validate function')
      //alert(this.name);
       //alert(event.name);
       var names = this.name
      var emails= this.email
      //alert('Call me');
      // var x = document.forms["myForm"]["Name"].value;
      //alert(document.forms["myForm"]["Name"].value);
      // var x = document.forms["myForm"]["Name"].value;
      //alert(this.$store.commit('updateMessage', e.target.value));

     if (names == '') {
        alert('Name must be filled out')
        return false
      } 
       else if(emails == ''){
         alert('Email must be filled out')
        return false
       }
      
      else {
        console.log(names)
        //document.write('Hello!'+x);
        //this.$router.push("/home?"+x);
        //this.$router.push({ path: 'home', query: { plan: 'private' }})
        this.$router.push({ name: 'home', params: { names, c: 'fuad',emails } })
        return true
      }
    },
    myFunction: function(p1, p2) {
      return p1 * p2
    }
  }
}
</script>

<style>
</style>
