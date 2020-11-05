<template>
    <b-form @submit.prevent="onSubmit" @reset="onReset" class="contact-form">
        <b-form-row>
            <b-col>
                <b-form-group
                label-for="input-1">
                    <b-form-input
                    v-model="company"
                    type="text"
                    required
                    placeholder="Company name">
                    </b-form-input> 
                </b-form-group>
            </b-col>
            <b-col>
                <b-form-group>
                    <b-form-select
                    v-model="option"
                    :options="options"
                    :value="null">
                    </b-form-select>
                </b-form-group>
            </b-col>
        </b-form-row>
        <b-form-row>
            <b-col>
                <b-form-group>
                    <b-form-input
                    v-model="email"
                    type="email"
                    required
                    placeholder="example@mail.com">
                    </b-form-input> 
                </b-form-group>
            </b-col>
            <b-col>
                <b-form-group>
                    <b-form-input
                    v-model="phone"
                    type="phone"
                    required
                    placeholder="example@mail.com">
                    </b-form-input> 
                </b-form-group>
            </b-col>
        </b-form-row>
        <b-form-row>
            <b-col>
                <b-textarea
                v-model="text"
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
            ]
        }
    },
    methods: {
        onSubmit(){
            
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