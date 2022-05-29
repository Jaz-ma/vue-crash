<template>
    <div @dblclick="$emit('toggle-reminder',task.id)" :class="[task.reminder? 'reminder': '', 'task']">

    <h3>
        {{task.text}}
        <i @click="onDelete(task.id)" class="fas fa-times"></i>
    </h3>
    <p>
        {{task.day}}
    </p>
    </div>
</template>

<script>

export default {
    name:'Task',
    props:{
        task: Object,
    },
    methods:{
      onDelete(id){
         this.$emit('delete-task',id)
      }
    },
}

</script>

<style scope>
.fas {
  color: red;
  cursor: pointer;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
-webkit-user-select: none; /* Safari */        
-moz-user-select: none; /* Firefox */
-ms-user-select: none; /* IE10+/Edge */
user-select: none; /* Standard */
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>