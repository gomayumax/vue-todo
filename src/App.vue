<template>
    <div id="app">
        <div class="colums">
            <div class="column is-half is-offset-one-quarter">
                <input-form ></input-form>
            </div>
        </div>
        <div class="colums">
            <div class="column is-half is-offset-one-quarter">
                <todo-list :todoList="todoList"></todo-list>
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
        {text: 'goma'}
      ],
      newTodo: ''
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
