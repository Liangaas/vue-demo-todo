<template>
    <div :class="['todo-item',todo.completed ? 'completed':'']">
        <input
            type="checkbox"
            class='toggle'
            v-model="todo.completed"
        >
        <label>{{todo.content}}</label>
        <button class="destory" @click="deleteTodo"></button>
    </div>
</template>
<script>
export default {
    props:{

    },
    methods:{
        deleteTodo(){
            //触发父组件的del事件名的事件
            this.$emit('del',this.todo.id)
        }
    }
}
</script>

