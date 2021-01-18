<template>
    <b-card 
    :title="service.name"
    :img-src="require(`@/assets/${service.image}`)"
    img-top
    tag="service">
    <b-card-text>
        {{service.description}}
    </b-card-text>
    </b-card>
</template>

<script>
export default {
    name: 'ServiceCard',
    props: ['service']
}
</script>

<style scoped>
    .card {
        max-height: 60vh;
    }
    .card-img-top {
        width: 100%;
        height: auto;
        max-height: 60%;
    }
    .card-title {
        font-size: 1rem;
        font-weight: bold;
    }
    .card-text {
        padding-bottom: 0.5em;
    }
    
</style>