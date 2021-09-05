<template>
    <div class="card mb-5">
        <div class="card-body">
            <h4 class="display-5 mb-4 font-weight-bold">Create a vacancy</h4>
            <form @submit.prevent="submit">
                <div class="form-group">
                    <input type="text" v-model="form.title" placeholder="Enter the job title" class="form-control" required>
                </div>
                <div class="form-group">
                    <input type="text" v-model="form.company" placeholder="Enter the company" class="form-control" required>
                </div>
                <div class="form-group">
                    <input type="text" v-model="form.city" placeholder="Enter the city" class="form-control" required>
                </div>
                <div class="form-group">
                    <textarea placeholder="Enter the job description" v-model="form.description"  cols="30" rows="5" class="form-control" required></textarea>
                </div>
                <div class="form-group">
                    <button type="submit" class="btn btn-dark btn-sm">Create</button>
                </div>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    name: 'newvacancies',
    data () {
        return {
            form:{
                'title':'',
                'company':'',
                'city':'',
                'description':'',
            }
        }
    },
    methods:{
        submit(){
            this.$emit('save',{...this.form,id:new Date().getTime().toString()})

            this.form.title='';
            this.form.company='';
            this.form.city='';
            this.form.description='';
        }
    }
}
</script>
<style>

</style>