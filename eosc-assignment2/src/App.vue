<script setup>
  import MessageEditor from "./components/MessageEditor.vue";
  import MessageFeed from "./components/MessageFeed.vue";
  import { ref } from "vue";

  let id = 0
  const messages = ref([])

  function addMessage(message) {
    messages.value.push({ id: id++, text: message})
  }
</script>

<template>
  <div class="messenger" align="center">
    <MessageFeed :messageFeed="messages" />
    <MessageEditor @sendText="(n) => addMessage(n)" />
  </div>
</template>

<style scoped>

</style>
