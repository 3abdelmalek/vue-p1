<template>
<div class="login-container">
    <h2>Login</h2>
    <form @submit.prevent="login">
        <div class="form-group">
            <label for="username">Username:</label>
            <input type="text" id="username" v-model="username" required />
        </div>
        <div class="form-group">
            <label for="password">Password:</label>
            <input type="password" id="password" v-model="password" required />
        </div>
        <button @click="showMsg" type="submit">Login</button>
    </form>
</div>
</template>

<script>
import BackgroundVue from './Background.vue';
export default {
    name: 'Login',
    data() {
        return {
            username: '',
            password: ''
        };
    },
    methods: {
        login() {
            // Perform login logic here
            console.log('Logging in with:', this.username, this.password);
            // You can add your authentication logic, e.g., sending a request to a server
        },
        showMsg() {
            if(this.username && this.password ) {
                if(this.username == "Hello " && this.password == "Luca" ) {
                    alert(this.username + this.password);
                } else{
                    alert("Wrong username or password");
                }
            }
        }
    }
};
</script>

<style scoped>
.login-container {
    color: black;
    max-width: 300px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.form-group {
    margin-bottom: 15px;
}

label {
    display: block;
    margin-bottom: 5px;
}

input {
    width: 100%;
    padding: 8px;
    box-sizing: border-box;
    margin-bottom: 10px;
}

button {
    background-color: #4caf50;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 3px;
    cursor: pointer;
}
</style>
