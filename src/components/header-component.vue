<template>
    <b-jumbotron>
        <section class="header-info">
            <h1 class="title">We want to help you grow</h1>
            <p class="description">
                In Ares Data we support your business by developing professional 
                solutions for your needs and data analysis.
            </p>
            <a href="#" class="btn ask-btn">Ask for help</a>
        </section>
    </b-jumbotron>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
    @media only screen and (max-width: 374px){
        .header-info {
            width: 100%;
        }
        .ask-btn {
            width: 50%;
        }
    }

    @media only screen and (min-width: 375px){
         .header-info {
            width: 60%; 
        }
        .ask-btn {
            width: 60%;
        }
    }

    @media only screen and (min-width: 768px){
        .ask-btn {
            width: 35%;
        }
    }

    @media only screen and (min-width: 1440px){
        .header-info {
            width: 40%;
        }
    }

    .jumbotron {
        height: 60vh;
        background-image: url('../assets/header-img.jpg');
        background-position: center center;
        background-size: cover;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
   
    .title, .description {
        filter: drop-shadow(0.5rem 0.5rem 0.5rem  rgb(75, 75, 75));
        font-weight: bold;
        color: whitesmoke;
    }
    .ask-btn {
        background-color: rgb(106, 185, 106);
        color: whitesmoke;
        font-weight: bold;
        border-radius: 0.5em;
        border: none;
    }
</style>