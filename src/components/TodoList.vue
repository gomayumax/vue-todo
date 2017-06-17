<template>
    <ul class="is-pulled-left">
        <li v-for="todo in todoList">
            <div class="field is-pulled-left">
                <b-checkbox v-model="todo.done">
                    {{ todo.text }}
                </b-checkbox>
                <button class="destroy" @click="removeTodo(todo)">
                    delete
                </button>
            </div>
        </li>
    </ul>
</template>

<script>
export default {
  name: 'todo-list',
  props: ['todoList'],
  methods: {
    removeTodo: function (todo) {
      this.$emit('removeTodo', todo)
    }
  }
}
</script>

