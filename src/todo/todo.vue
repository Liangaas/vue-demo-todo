<template>

    <section class="real-app">
    <input
    type='text'
    class='add-input'
    autofocus='autofocus'
    placeholder='记录待办事项'
    @keyup.enter='addTodo'
    >
    
    
    </section>
</template>
<script>
import Item from './item.vue'
let id = 0
export default {
    data(){
        return{
            todos:[]
        }
    },
    components:{
      
    },
    computed:{

    },
    methods:{
        addTodo(e){
            this.todos.unshift({
                id:id++,
                content:e.target.value.trim(),
                computed:false
            })
            e.target.value=''
        }
    },
    beforeCreate:function(){
        console.log('before create')
    },
    created:function(){
        console.log('create ')
    
    },
    beforeMount:function(){
        console.log('beforeMount')
    },
    mounted:function(){
        console.log('mounted')
    },
    beforeUpdate:function(){
        console.log('before update')
    },
    updated:function(){
        console.log('updated ')
    },
    beforeDestroy:function(){
        console.log('before destroy')
    },
    destroyed:function(){
        console.log('destory')
    }
}
</script>
<style>
.real-app{
    widows:600px;
    margin:0 auto;
    box-shadow:0 0 5px #666;
}
.add-input{
   position: relative;
    margin: 0;
    width: 100%;
    font-size: 24px;
    font-family: inherit;
    font-weight: inherit;
    line-height: 1.4em;
    border: 0;
    outline: none;
    color: inherit;
    padding: 6px;
    border: 1px solid #999;
    box-shadow: inset 0 -1px 5px 0 rgba(0, 0, 0, 0.2);
    box-sizing: border-box;
    font-smoothing: antialiased;
    padding: 16px 16px 16px 60px;
    border: none;
    box-shadow: inset 0 -2px 1px rgba(0,0,0,0.03);
    
}
</style>

