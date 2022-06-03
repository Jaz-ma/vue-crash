<template>
    <header>
        <h1>{{title}}</h1>
        <Button v-show="homePage" @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Zid Task'" :color="showAddTask ? 'red' :'green'"/>
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
    },
    computed:{
        homePage(){
            if(this.$route.path==='/'){
                return true
            }else{
                return false
            }
        }
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