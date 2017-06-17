<template>
    <div id="app">
        <div class="container" >
            <div class="colums">
                <div class="column is-half is-offset-one-quarter
">
                    <input-form @addTodo="addTodo"></input-form>
                </div>
            </div>
            <div class="colums">
                <div class="column is-half is-offset-one-quarter
">
                    <todo-list :todoList="todoList"
                               @removeTodo="removeTodo"
                    ></todo-list>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
  import Hello from './components/Hello'
  import InputForm from './components/InputForm'
  import TodoList from './components/TodoList'

  export default {
    name: 'app',
    components: {
      Hello,
      InputForm,
      TodoList
    },
    data: function () {
      return {
        todoList: [
          {text: 'goma', done: false}
        ]
      }
    },
    methods: {
      addTodo: function (todo) {
        this.todoList.push({
          text: todo,
          done: false
        })
      },
      removeTodo: function (todo) {
        this.todoList.splice(this.todoList.indexOf(todo), 1)
      }
    }
  }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
