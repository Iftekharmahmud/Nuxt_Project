<template>
    <div>
        <!--<h1>posts/:id route</h1>-->
        <h1>posts/{{$route.params.id}} route</h1>
        <button @click="popup">Press</button>
    </div>
</template>
<script>
export default{
methods:{
    popup(){
        alert(this.$route.params.id)
    }
}

}

</script>