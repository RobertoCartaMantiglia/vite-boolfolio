<template>
    <div>
        <h1 class="text-center">SinglePost</h1>
        <div class="col-5 project-card my-2 p-2 border border-dark rounded">
            <img :src="`http://127.0.0.1:8000/storage/${project.thumb}`" class="card-img-top img-fluid" alt="#">
            <div class="card-body">
                <h5 class="card-title mb-2">{{ project.title }}</h5>
                <p class="card-text">{{ project.description }}</p>

            </div>
        </div>
    </div>
</template>


<script>

import ProjectComponent from '../components/ProjectComponent.vue';
import axios from 'axios';


export default {
    name: 'SinglePost',
    components: {
        ProjectComponent
    },
    data() {
        return {
            urlAddress: 'http://127.0.0.1:8000'
        }
    },
    methods: {
        getProject() {
            axios.get(this.urlAddress + `/api/projects/${this.$route.params.id}`, {

            })
                .then((response) => {
                    this.project = response.data.result;
                    console.log(response);
                })
                .catch(function (error) {
                    console.log(error);
                });
        }
    },
    created() {
        this.getProject();
    }
}

</script>
<style lang="scss" scoped></style>