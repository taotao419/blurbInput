<template>
  <div>
    <BlurbInputText></BlurbInputText>

    <el-input v-model="input" placeholder="Please input text"></el-input>
  </div>
</template>

<script>
import BlurbInputText from "./BlurbInputText.vue";

let nextTodoId = 1;

export default {
  components: {
    BlurbInputText,
  },
  data() {
    return {
      newTodoText: "",
      todos: [
        {
          id: nextTodoId++,
          text: "Learn Vue"
        },
        {
          id: nextTodoId++,
          text: "Learn about single-file components"
        },
        {
          id: nextTodoId++,
          text: "Fall in love"
        }
      ]
    };
  },
  methods: {
    addTodo() {
      const trimmedText = this.newTodoText.trim();
      if (trimmedText) {
        this.todos.push({
          id: nextTodoId++,
          text: trimmedText
        });
        this.newTodoText = "";
      }
    },
    removeTodo(idToRemove) {
      this.todos = this.todos.filter(todo => {
        return todo.id !== idToRemove;
      });
    }
  }
};
</script>