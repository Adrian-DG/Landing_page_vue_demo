<template>
    <b-container fluid="md">
        <b-row>
            <b-col md="12">
                <h3 class="title">Testimonies</h3>
                <hr/>
            </b-col>
        </b-row>
        <b-row>
            <b-col class="item" sm="12" md="8" lg="6" v-for="(testimonie,index) in testimonies" :key="index">
                <TestCard :testimonie="testimonie"/>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
import TestCard from './testimonies-card-component';

export default {
    name: 'Testimonies',
    components: { TestCard },
    data: function(){
        return {
            testimonies: [
                {
                    image: 'kure-logo.svg',
                    company: 'Kure',
                    text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.`
                },
                 {
                    image: 'topcon-logo.svg',
                    company: 'Topcon',
                    text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.`
                },
                 {
                    image: 'kure-logo.svg',
                    company: 'Kure',
                    text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.`
                }
            ]
        }
    }
}
</script>

<style scoped>
    .container {
        margin: 3em auto 2em auto;
    }
    .title {
        text-align: center;
    }

    .item {
        margin-bottom: 1em;
    }

</style>