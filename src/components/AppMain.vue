<script>
import axios from 'axios';
import ProjectComponent from './ProjectComponent.vue';
export default {
    name: 'Appmain',
    components: {
        ProjectComponent
    },
    data() {
        return {
            projects: [],
            urlAddress: 'http://127.0.0.1:8000/api/projects/'
        }
    },
    methods: {
        getProject() {
            axios.get(this.urlAddress, {
                params: {

                }
            })
                .then((response) => {

                    this.projects = response.data.result.data;
                })
                .catch(function (error) {
                    console.log(error);
                })

        }
    },
    created() {
        this.getProject();
    },
}

</script>

<template>
    <section>
        <div class="container">
            <div class="row  justify-content-around">
                <h1 class="text-center">MyProjects</h1>
                <ProjectComponent v-for="project in projects" :projectTitle="project.title"
                    :projectDescription="project.description" />
                <!-- <div class="col-5 project-card m-2 p-2 border border-dark" v-for="project in projects">                       
                                        <img :src="project.thumb" class="card-img-top" alt="#">
                                        <div class="card-body">
                                            <h5 class="card-title">{{project.title}}</h5>
                                            <p class="card-text">{{project.description.substr(0, 100)}}</p>
                                            <a href="#" class="btn btn-primary">Show more</a>
                                        </div> -->
            </div>
        </div>
    </section>
</template>

<style  lang="scss" scoped></style>