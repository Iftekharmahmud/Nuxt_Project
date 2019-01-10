<template>
  <section class="container">
  
    <h1>Welcome</h1>
    <table>
       <tr>
    <th>Name</th>
    <th>Email</th>
     </tr>
      <tr>
    <td>{{ name }}</td>
    <td></td>
  </tr>
  

   <!-- <h1>{{ this.$route.params.names }}</h1>-->
    
    <!--<h1>{{ this.$route.params.c }}</h1>-->
    </table>
  </section>
</template>

<script>
export default {
  data() {
    return {
      mydata: 'hello111',
      title: 'iftekhar',
     // name: localStorage.getItem("Na"),
      name: '',
      email:''

    }
  },
 mounted() {
    
     /* this.name = this.$route.params.names;
     // this.email= this.$route.params.emails;
      localStorage.setItem("Na", name);
      console.log(localStorage.getItem("Na"));
       var nx=localStorage.getItem("Na");
      //localStorage.setItem("Em",email);*/

    
  },
    /*watch: {
    name(newName) {
      localStorage.name = newName;
    }
  },*/
   beforecreated: function() {
    /*console.log('this is beforecreated ')
     this.name = this.$route.params.names;
     // this.email= this.$route.params.emails;
      localStorage.setItem("Na", name);
      console.log(localStorage.getItem("Na"));
       var nx=localStorage.getItem("Na");*/

  },
   beforeMount: function() {
    // `this` points to the vm instance
    console.log('this is beforeMount ')
  },
  beforeUpdate(){
    console.log('this is beforeUpdate ')
  },
   beforeDestroy(){
    console.log('this is beforeDestroy ')
    /* this.name = this.$route.params.names;
     // this.email= this.$route.params.emails;
      localStorage.setItem("Na", this.$route.params.names);
      console.log(localStorage.getItem("Na"));
       var nx=localStorage.getItem("Na");*/

  },
   destroyed(){
    console.log('this is destroyed ')
  },

  created(){

      if(localStorage.getItem("Na") !='' && localStorage.getItem("Na")!='undefined'){
         this.name = localStorage.getItem("Na");
      }
      else{
      this.name = this.$route.params.names;
      localStorage.setItem("Na", this.$route.params.names);
      }
     // this.email= this.$route.params.emails;
      //localStorage.setItem("Na", this.$route.params.names);
      console.log(localStorage.getItem("Na"));
       var nx=localStorage.getItem("Na");


  }
}
</script>
<style>
table, th, td {
    border: 1px solid black;
}
</style>
