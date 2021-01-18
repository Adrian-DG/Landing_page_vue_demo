<template>
    <b-form @submit.prevent="onSubmit" class="contact-form" v-if="show">
        <b-form-row>
            <b-col>
                <b-form-group
                label-for="input-1">
                    <b-form-input
                    v-model="request.company"
                    required
                    placeholder="Company name">
                    </b-form-input> 
                </b-form-group>
            </b-col>
            <b-col>
                <b-form-group>
                    <b-form-select
                    v-model="request.option"
                    :options="options"
                    required>
                    </b-form-select>
                </b-form-group>
            </b-col>
        </b-form-row>
        <b-form-row>
            <b-col>
                <b-form-group>
                    <b-form-input
                    v-model="request.email"
                    type="email"
                    required
                    placeholder="example@mail.com">
                    </b-form-input> 
                </b-form-group>
            </b-col>
            <b-col>
                <b-form-group>
                    <b-form-input
                    v-model="request.phone"
                    type="phone"
                    required
                    placeholder="Phone number">
                    </b-form-input> 
                </b-form-group>
            </b-col>
        </b-form-row>
        <b-form-row>
            <b-col>
                <b-textarea
                v-model="request.text"
                rows="3"
                max-rows="5"
                placeholder="Enter something"></b-textarea>
            </b-col>
        </b-form-row>
        <b-row>
            <b-col>
                <b-button type="submit" block variant="success" class="">Let us know</b-button>
            </b-col>
        </b-row>
    </b-form>
</template>

<script>
export default {
    name: 'ContactForm',
    data: function(){
        return {
            request: {
                company: '',
                option: null,
                email: '',
                phone: '',
                text: ''
            },
            options: [
                {
                    text: 'Choose',
                    value: null
                },
                'Enterprise Software',
                "I've problems analysing data",
                'I need a mobile app',
                'Social network marketing',
                'I need a custom solution'
            ],
            show: true
        }
    },
    methods: {
        onSubmit(event){
            event.preventDefault();
            alert(JSON.stringify(this.request));
        }
    }    
}
</script>

<style scoped>
    .contact-form {
        width: 100%;
        height: 100%;
        background-color: #EEEEEE;
        border-radius: 0.5em;
        padding: 1em;
    }
    .row{
        margin-top: 1em;
    }

</style>