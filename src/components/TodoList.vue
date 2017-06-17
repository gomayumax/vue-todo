<template>
    <ul>
        <li v-for="item in items">
            {{ item.text }}
        </li>
    </ul>
</template>

<script>
export default {
  name: 'todo-list',
  data: function () {
    return {
      items: [
        {text: 'Foo'},
        {text: 'Bar'}
      ]
    }
  }
}
</script>

