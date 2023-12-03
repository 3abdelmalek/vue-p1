<!-- App.vue -->

<script>
// Import the Hello component from './components/Hello.vue'
import Background from './components/Background.vue';
// Export the App component
export default {
    name: 'App', // Component name
    components: {
        Background,
    }
}
</script>

<template>
    <Background />
</template>
<style>
/* Your styles go here */
</style>
