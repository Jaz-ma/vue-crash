<template>
    <header>
        <h1>{{title}}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Zid Task'" :color="showAddTask ? 'red' :'green'"/>
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
        showAddTask: Boolean,
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