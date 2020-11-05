<template>
    <b-card no-body>
        <b-row>
            <b-col md="4" class="img-container">
                <b-card-img class="card-img" :src="require(`@/assets/${testimonie.image}`)"/>
            </b-col>
            <b-col md="8">
                <b-card-body :title="testimonie.company">
                    <b-card-text>
                        {{ testimonie.text }}
                    </b-card-text>
                </b-card-body>
            </b-col>
        </b-row>
    </b-card>    
</template> 

<script>
export default {
    name: 'TestCard',
    props: ['testimonie']
}
</script>

<style scoped>
    @media only screen and (max-width: 767px){
        .img-container {
            border-right: none;
            border-bottom: 1px solid gainsboro;
        }
    }

    @media only screen and (min-width: 768px) {
        .img-container {
            border-right: 1px solid gainsboro;
        }
    }

    .img-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;        
    }
    .card-img {
        width: 90%;
        height: auto;
        margin: auto;
    }
</style>