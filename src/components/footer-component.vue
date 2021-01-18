<template>
    <b-row fluid class="footer">
        <b-col md="6">
            <img class="img-fluid" :src="require(image)"/>
        </b-col>
        <b-col md="6">
            <ul class="navbar-nav">
                <li class="nav-item" v-for="n in 5" :key="n">
                    <a class="nav-link">Link</a>
                </li>
            </ul>
        </b-col>
    </b-row>
</template>

<script>
export default {
    name: 'Footer',
    data: function(){
        return {
            image: '@/assets/maps.jpeg'
        }
    }
}
</script>

<style scoped>
    .footer {
        width: 100%;
        height: 30vh;
        background-color: #343a40;
    }
</style>