<template>
    <div class="container col-md-6 d-flex flex-column justify-content-center">
        <div id="vacancies" class="py-5">
            <section>
                <h4 class="display-5 font-weight-bold">Find your dream job today</h4>
                <p class="display-6 text-muted">Apply for any vacancies below</p>
            </section>
        </div>
        <new-vacancy @save="SaveJob"/>
        <vacancy v-for="vacancy in vacancies" :key="vacancy.id" :vacancy='vacancy'/>
    </div>
</template>
<script>
import NewVacancy from '../components/NewVacancy';
import Vacancy from '../components/Vacancy';
import {vacancies} from '../../data';

export default {
    name: 'home',
    data () {
        return {
            vacancies,
        }
    },
    components:{
        NewVacancy,
        Vacancy,
    },
    methods:{
        SaveJob(FormData){
            console.log('form data',FormData);
            this.vacancies.unshift(FormData)
        }
    }
}
</script>
<style>

</style>