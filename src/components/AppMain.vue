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
                <!-- <h1 class="text-center">MyProjects</h1> -->
                <ProjectComponent v-for="project in projects" :projectTitle="project.title"
                    :projectDescription="project.description.substr(0, 200)" />
            </div>
        </div>
    </section>
</template>

<style  lang="scss" scoped></style>