<template>
  <div>
    <BaseMessageText v-model="newTodoText" placeholder="Enter Message" @keydown.enter="addTodo" />
    <ul v-if="todos.length">
      <MessageListItem v-for="todo in todos" :key="todo.id" :todo="todo" />
    </ul>
    <p v-else>Welcome To Messaging App!.</p>
  </div>
</template>

<script>
import BaseMessageText from "./BaseMessageText.vue";
import MessageListItem from "./MessageListItem.vue";

let nextTodoId = 1;

export default {
  components: {
    BaseMessageText,
    MessageListItem
  },
  data() {
    return {
      newTodoText: "",
      todos: []
    };
  },
  methods: {
    addTodo() {
      const trimmedText = this.newTodoText.toLowerCase();
      if (trimmedText) {
        this.todos.push({
          id: nextTodoId++,
          text: trimmedText
        });
        this.newTodoText = "";
      }
    }
  }
};
</script>