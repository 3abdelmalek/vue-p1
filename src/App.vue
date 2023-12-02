<!-- App.vue -->

<script>
// Import the Hello component from './components/Hello.vue'
import Hello from './components/Hello.vue';

// Export the App component
export default {
    name: 'App', // Component name
    components: {
        Hello // Register the Hello component for use in this component
    }
}
</script>

<template>
<!-- Use the Hello component within the template -->
<Hello />
</template>

<style>
/* Your styles go here */
</style>
