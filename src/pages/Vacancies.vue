<template>
<div class="container col-md-6 d-flex flex-column justify-content-center mt-5">
 <div class="card mb-5" v-for="vacancy in vacancies" :key="vacancy.id">
        <div class="card-body">
            <h4 class="display-5 font-weight-bold">{{ vacancy.title }}</h4>
            <span class="text-muted">{{ vacancy.company }}</span>
            <p>{{ vacancy.city }}</p>
            <p class="text-dark">
                {{ vacancy.description }}
            </p>
            <form>
                <div class="form-group">
                    <button type="submit" class="btn btn-dark btn-sm">Apply</button>
                </div>
            </form>
        </div>
    </div>
</div>
</template>
<script>
import {vacancies} from '../../data';

export default {
    name: 'vacancies',
    data () {
        return {
            vacancies
        }
    }
}
</script>
<style>

</style>