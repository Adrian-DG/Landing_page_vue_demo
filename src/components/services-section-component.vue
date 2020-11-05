<template>
    <b-row class="container">
        <b-col fluid="md">
            <b-row>
                <b-col>
                    <h3 class="title">Our Services</h3>
                    <hr/>
                </b-col>
            </b-row>
            <b-row class="services-list">
                <b-col sm="9" md="4" lg="3" class="service-item" v-for="(service,index) in services" :key="index">
                    <ServiceCard :service="service"/>
                </b-col>
            </b-row>
        </b-col>
    </b-row>
</template>

<script>
import ServiceCard from "./services-card-component";

export default {
  name: "Services",
  components: { ServiceCard },
  data: function () {
    return {
      services: [
        {
          image: "service.jpg",
          name: "Mobile Development",
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. `,
        },
        {
          image: "service.jpg",
          name: "Enterprise Application",
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. `,
        },
        {
          image: "service.jpg",
          name: "Cyber Security Assesory",
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. `,
        },
        {
          image: "service.jpg",
          name: "Mobile Development",
          description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. `,
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  margin: auto;
}
.title {
  text-align: center;
}
.services-list {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}

.service-item {
  margin-bottom: 1em;
}
</style>