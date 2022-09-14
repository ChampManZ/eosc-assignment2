<script setup>
    import { ref } from 'vue'

    const message = ref('')

    function resetMessage() {
        message.value = ''
    }
</script>

<template>
    <div class="textfield">
        <textarea class="textCenter" v-model="message" placeholder="Type here..."></textarea> <br>
        <button @click="$emit('sendText', message); resetMessage()">Send</button>
    </div>
</template>

<style scoped>

</style>