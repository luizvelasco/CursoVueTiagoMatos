<template>
    <div>
        {{fullName}}
        <h2>Todos em aberto</h2>
        <div v-for="todo in unConmpletedTodo" :key="todo.id">
            {{todo.title}} 
        </div>
        <h2>Todos completas</h2>
         <div v-for="todo in conmpletedTodo" :key="todo.id">
            {{todo.title}} 
        </div>
        <h2>Todas Todos</h2>
         <div v-for="todo in todos" :key="todo.id">
            <input type="checkbox" v-model="todo.completed">{{todo.title}}
        </div>

    </div>
</template>

<script>
export default {
    name: 'PropriedadeComputada',
    data() {
        return {
            user: {
                first_name: 'Jon',
                last_name: 'Snow'
            },
            todos: [
                {
                userId: 1,
                id: 1,
                title: "delectus aut autem",
                completed: true
                },
                {
                userId: 1,
                id: 2,
                title: "quis ut nam facilis et officia qui",
                completed: false
                },
                {
                userId: 1,
                id: 3,
                title: "fugiat veniam minus",
                completed: false
                },
                {
                userId: 1,
                id: 4,
                title: "et porro tempora",
                completed: true
                },
                {
                userId: 1,
                id: 5,
                title: "laboriosam mollitia et enim quasi adipisci quia provident illum",
                completed: false
                }
            ]
        }
    },
    computed: {
        fullName(){
            return `${this.user.first_name} ${this.user.last_name}`  
        },
        unConmpletedTodo(){
            return this.todos.filter(todo => !todo.completed);
        },
        conmpletedTodo(){
            return this.todos.filter(todo => todo.completed);
        }
    },
    methods: {
       
    }
}
</script>