<template>
    <b-field label="Todo: ">
        <b-input placeholder="todoを入力してください"
                 v-model="newTodo"
        ></b-input>
        <button @click="addTodo">add</button>
    </b-field>
</template>

<script>
export default {
  name: 'input-form',
  data: function () {
    return {
      newTodo: ''
    }
  },
  methods: {
    addTodo: function () {
      this.$emit('addTodo', this.newTodo)
      this.newTodo = ''
    }
  }
}
</script>

