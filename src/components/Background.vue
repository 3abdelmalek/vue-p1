<template>
<div :style="{ backgroundColor: bgColor }">
    <button @click="toggleBackground" >{{ btnName }}</button>
    <Login/>
</div>
</template>

<script>
import Login from './Login.vue';
export default {
    components: {
        Login,
    },
    name: 'Background',
    data() {
        return {
            isDarkMode: false
        };
    },
    computed: {
        // Computed property to dynamically set the background color
        bgColor() {
            return this.isDarkMode ? 'black' : 'white';
        },
        // Computed property to dynamically set the name of next background
        btnName() {
            return this.isDarkMode? 'Light Mode' : 'Dark Mode';
        }
    },
    methods: {
        // Method to toggle between dark and light mode
        toggleBackground() {
            this.isDarkMode = !this.isDarkMode;
        }
    }
};
</script>

<style>
/* You can add component-specific styles here if needed */
div {
    padding: 20px;
    text-align: center;
    width: 100%;
}

button {
    padding: 10px;
    font-weight: bold;
}
</style>
