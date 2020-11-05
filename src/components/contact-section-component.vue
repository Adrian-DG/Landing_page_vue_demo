<template>
    <b-container>
        <b-row>
            <b-col md="12">
                <h3 class="title">Contact Us</h3>
                <hr/>
            </b-col>
        </b-row>
        <b-row fluid="md">
            <b-col lg="6" class="col-img">
                <img class="form-img" :src="require(`@/assets/${image}`)"/>
            </b-col>
            <b-col lg="6" md="12">
                <b-row class="greet">
                    <b-col>
                        <p>Feel free to contact us and ask all the questions you need to.</p>
                        <h4>Remenber we are here to help you</h4>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col>
                        <ContactForm/>
                    </b-col>
                </b-row>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
import ContactForm from './contact-form-component';

export default {
    name: 'Contact',
    components: { ContactForm },
    data: function() {
        return {
            image: 'contact-img.jpg'
        }
    }
}
</script>

<style scoped>
    .form-img {
        width: 100%;
        height: auto;
        border-radius: 0.5em;
    }

    .title {
        text-align: center;
    }

    @media only screen and (max-width: 1023px){
        .form-img {
            margin-bottom: 1em;
        }
    }

    @media only screen and (max-width: 1439px) {
        .greet {
            display: none;
        }        
    }

</style>