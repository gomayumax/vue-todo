<template>
    <ul>
        <li v-for="todo in todoList">
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

