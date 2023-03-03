<script>

export default {
    name: 'ProjectComponent',
    props: [
        'projectTitle',
        'projectDescription',
    ],
    data() {
        return {

        }
    },
    methods: {

    },

}

</script>

<template>
    <div class="col-5 project-card my-2 p-2 border border-dark rounded">
        <!-- <img :src="project.thumb" class="card-img-top" alt="#"> -->
        <div class="card-body">
            <h5 class="card-title mb-2">{{ projectTitle }}</h5>
            <p class="card-text">{{ projectDescription }}</p>
            <a href="#" class="btn btn-primary">Show more</a>
        </div>
    </div>
</template>

<style  lang="scss" scoped></style>