<template>
<div class="container">
    <nav :class="[`bg-${theme}`, `navbar-${theme}`]" class="navbar navbar-expand-lg">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Meat-Store</a>
            <div>
            <button @click.prevent="changeTheme" type="button" :class="[`text-${nextTheme()}`, `border-${nextTheme()}`]" class="btn mx-1">
                    {{ nextTheme().charAt(0).toUpperCase() + nextTheme().substring(1) }}
            </button>







                
                <button class=" mx-1 navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
            </div>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Home</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                            Meat
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                            <li><a class="dropdown-item" href="#">Normal Meat</a></li>
                            <li><a class="dropdown-item" href="#">Monster Meat</a></li>
                            <li><a class="dropdown-item" href="#">Mini Meat</a></li>
                        </ul>
                    </li>
                </ul>
                <form class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                    <button :class="[`btn btn-outline-${nextTheme()}`]" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>

    <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="https://picsum.photos/id/222/200" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img src="https://picsum.photos/id/239/200" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img src="https://picsum.photos/id/200/200" class="d-block w-100" alt="...">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden"></span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden"></span>
        </button>
    </div>
    <div class="input-group flex-nowrap my-2">
        <span class="input-group-text" id="addon-wrapping">@</span>
        <input v-model="name" type="text" class="form-control" placeholder="name" aria-label="Username" aria-describedby="addon-wrapping">
    </div>
    <div class="input-group mb-3">
        <span class="input-group-text" id="basic-addon3">example.com</span>
        <input v-model="email" type="text" class="form-control" id="basic-url" aria-describedby="basic-addon3">
    </div>
    <button @click="showMsg" class="btn btn-outline-primary px-4 " type="submit" value="Submit"> Send </button>
</div>
</template>

<script>
export default {
    name: 'Hello',
    data() {
        return {
            name: '',
            email: '',
            theme: 'light',
            navbarAtt: []
        }
    },
    methods: {
        nextTheme() {
            return this.theme == 'light' ? 'dark' : 'light';
        },
        changeTheme() {
            let theme = 'light'
            if(this.theme == 'light'){
                theme = 'dark'
            }
            this.theme = theme
        },
        showMsg() {
            if(this.userName && this.email ) {
                alert("Did You Want Some Monster Meat (#4) :)")
            }
        }
    },
}
</script>

<style>
</style>
