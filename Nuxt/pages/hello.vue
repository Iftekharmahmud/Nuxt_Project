<template>
  <section class="container">
    {{ mydata }} <h1>{{ title }}</h1> 
    <!--<h1>{{this.$store.commit('increment')}}</h1>-->
    <button @click="$store.commit('increment')">{{ $store.state.counter }}</button>
  </section>
</template>

<script>
export default {
  data() {
    //alert('Hi');
    console.log('export default data')
    //return this.$store.commit('increment')
    //$store.commit('increment')
    //console.log(this.$store.state.count)
    return {
      mydata: 'Hello',
      title: 'iftekhar'
    }
  },
  mounted() {
    console.log('this is mounted ')
    console.log(this.$store.state.counter)
    this.$store.commit('increment')
    console.log(this.$store.state.counter)
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
  }
  /*mounted: function () {
    // `this` points to the vm instance
    console.log('this is mounted ' )
    console.log(this.$store.state.counter)
    this.$store.commit('increment')
    console.log(this.$store.state.counter)
    //console.log(this.$store.state.count)
    //console.log(this.$store.commit('increment'))
  }*/
}
</script>
