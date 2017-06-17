<template>
    <ul>
        <li v-for="todo in todoList">
            <b-checkbox v-model="todo.done"></b-checkbox>
            {{ todo.text }}
        </li>
    </ul>
</template>

<script>
export default {
  name: 'todo-list',
  props: ['todoList']
}
</script>

