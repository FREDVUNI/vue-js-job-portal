<template>
    <div class="card mb-5">
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
</template>
<script>
export default {
    name: 'Vacancy',
    props:['vacancy'],
    data () {
        return {
        }
    }
}
</script>
<style>

</style>