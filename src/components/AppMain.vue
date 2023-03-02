<script>
import axios from 'axios';
export default {
    name: 'Appmain',
    data() {
        return {
            project: [],
            urlAddress: 'http://127.0.0.1:8000/api/projects/'
        }
    },
    methods: {
        getProject() {
            axios.get(this.urlAddress, {
                params: {

                }
            })
                .then(function (response) {
                    console.log(response.data.result.data);
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

<template lang="">
    <div>
        <h1>ciao</h1>
    </div>
</template>

<style  lang="scss" scoped></style>