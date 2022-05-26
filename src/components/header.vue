<template>
    <header>
        <h1>{{title}}</h1>
        <Button text="Zid Task" color="green"/>
    </header>
</template>

<script>
import Button from './button.vue'
export default{
    name:"Header",
    components:{
        Button
    },
    props:{
        title: String,
    }
}


</script>

<style scoped>
header{
    display:flex;
    align-items: center;
    margin-bottom: 20px;
    justify-content: space-between;
}
</style>