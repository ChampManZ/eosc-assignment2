<script setup>
    const props = defineProps({
        messageFeed: Array
    })
</script>

<template>
    <div>
        <p v-for="i in messageFeed" :key="i.id">{{ i.text }}</p>
    </div>
</template>