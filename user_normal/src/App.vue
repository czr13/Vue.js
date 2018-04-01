import './assets/todos.less'
<template>
    <div id="app">
        <h1>{{title}}</h1>
        <ul>
            <li v-for="(todo,index) in todos" :id="index">
                <label>{{todo.value}}.{{index}}</label>
            </li>
        </ul>
    </div>

</template>


<script>

    /* 首先，在组件脚本定义中使用data定义用于内部访问的数据模型 */
    /* data可以是一个返回Object对象的函数，也可以是一个对象属性，也就是说，可以写成以下的方式  */
    /*export default{
        ...
        data:{
        title:"vue-todos"
        }
    } */
     export default{
        name:'app',
        data () {
         return {
            title:"vue-todos",
            todos:[
                {value:"阅读一本关于前端开发的书",done:false},
                {value:"补充范例代码",done:true},
                {value:"写心得",done:false},
            ]
         }
        }
     }

</script>
<style>
</style>