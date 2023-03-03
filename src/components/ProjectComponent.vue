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
    <div>
        <div class="col-4 project-card m-2 p-2 border border-dark">
            <!-- <img :src="project.thumb" class="card-img-top" alt="#"> -->
            <div class="card-body">
                <h5 class="card-title">{{ projectTitle }}</h5>
                <p class="card-text">{{ projectDescription }}</p>
                <a href="#" class="btn btn-primary">Show more</a>
            </div>
        </div>
    </div>
</template>

<style  lang="scss" scoped></style>