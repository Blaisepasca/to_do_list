<template>
    <div class="home">

        <div class="day">
            <div class="todotext">
                Today's To Do
            </div>
            <img src="../assets/process_30px.png" width="20" height="20">
        </div>

        <form @submit.prevent="submit">
            <div class="addlist">
                <input type="text" placeholder=" Add to your list .." v-model="form.addTodo">
                <button type="submit">
                    <img src="../assets/logout_30px.png" width="20" height="20px">
                </button>
            </div>
        </form>
        <div class="todos">
            <div v-for="index in todos" :key="index">
                <TodoitemsComponents :isChecked='index.ischecked' :name="index.name" :delete="index.delete" />
            </div>
        </div>
        <div class="clear">
            Clear all completed
        </div>
    </div>
</template>

<script>
import TodoitemsComponents from './TodoitemsComponents.vue'

export default {
    name: 'HomeComponents',
    components: {
        TodoitemsComponents
    },
    data() {
        return {
            form: {
                addTodo: ''
            },
            todos: []
        }
    },
    methods: {
        submit() {
            let gettodo = this.form.addTodo
            this.todos.push({
                ischecked: false,
                name:gettodo,
                delete:false
            })
        }
    },


}
</script>

<style>
.home {
    width: 500px;
    height: auto;
    min-height: 350px;
    margin: auto;
    margin-top: 150px;
    background-color: #FCFCFC;

}

.day {
    width: 100%;
    height: 60px;
    line-height: 50px;
    border-bottom: 2px solid #404040;
    display: inline-flex;
    justify-content: space-between;


}

.todotext {
    margin-left: 3px;
}

.addlist {
    height: 40px;
    line-height: 50px;
    border-bottom: 2px solid #404040;
    display: inline-flex;
    justify-content: space-between;
    width: 100%;


}

.todos {
    height: auto;
    min-height: 200px;
    border-bottom: 2px solid #404040;

}

.clear {
    height: 50px;
    width: 100%;
    background-color: #8F8F8F;
    text-align: center;
    line-height: 50px;
    color: white;

}

input {
    height: 60%;
    width: 90%;
    border: none;
    outline: none;

}

button {
    background-color: #FCFCFC;
    border: none;
    height: 20px;
    width: 20px;
    margin-right: 20px;
}
</style>
