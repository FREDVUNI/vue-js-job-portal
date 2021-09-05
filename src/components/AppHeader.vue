<template>
    <div id="app">
        <nav class="navbar navbar-expand-md navbar-light bg-white shadow-sm fixed-top">
            <div class="container">
                <router-link to="/" class="navbar-brand">JOB PORTAL</router-link>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="{{ __('Toggle navigation') }}">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav mr-auto">
                        <li class="nav-item">
                            <router-link to='/' class="nav-link">Home</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link to='/vacancies' class="nav-link">Vacancies</router-link>
                        </li>
                    </ul>
                    <ul class="navbar-nav ml-auto">
                        <li class="nav-item">
                            <router-link to='/' class="nav-link">Sign up</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link to='/vacancies' class="nav-link">Log in</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav> 
    </div>
</template>
<script>
export default {
    name: 'appheader',
    data () {
        return {
        }
    }
}
</script>
<style>

</style>