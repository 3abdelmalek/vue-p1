<!-- components/Hello.vue -->

<script>
// The script section of the Hello component
export default {
    name: 'Hello', // Component name
    data() {
        // Data function returns the initial data for the component
        return {
            msg: 'Hello ',
            name: 'Luca'
        };
    }
}
</script>

<template>
<!-- The template section contains the HTML structure of the component -->
<div> {{ msg + name }} </div>
</template>

<style>
/* Styles specific to the Hello component go here */
</style>
