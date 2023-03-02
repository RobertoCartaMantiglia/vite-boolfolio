<script>

export default {
    name: 'ProjectComponent',
    data() {
        return {

        }
    },
    methods: {

    },

}

</script>

<template lang="">
    <div class="col-5 project-card m-2 p-2 border border-dark" v-for="project in projects">                       
        <img :src="project.thumb" class="card-img-top" alt="#">
        <div class="card-body">
            <h5 class="card-title">{{project.title}}</h5>
            <p class="card-text">{{project.description.substr(0, 100)}}</p>
            <a href="#" class="btn btn-primary">Show more</a>
        </div>
    </div>
</template>

<style  lang="scss" scoped></style>