<template>
  <div>
    <Header />
    <Banner />
    <Advantages />
    <Availability :data="availabilityData" />
    <AboutUs />
    <AboutManufacture />
    <Form />
    <OurPartners />
    <Reviews :data="reviewsData" />
    <Map />
    <Footer />
    <router-view />
  </div>
</template>

<script>
import Header from "./components/TheHeader.vue";
import Banner from "./components/TheBanner.vue";
import Advantages from "./components/AppAdvantages.vue";
import Availability from "./components/AppAvailability.vue";
import AboutUs from "./components/AppAboutUs.vue";
import AboutManufacture from "./components/AppAboutManufacture.vue";
import Form from "./components/AppForm.vue";
import OurPartners from "./components/AppOurPartners.vue";
import Reviews from "./components/AppReviews.vue";
import Map from "./components/AppMap.vue";
import Footer from "./components/AppFooter.vue";
import { reviewsData, availabilityData } from "./data/data.app";
export default {
  components: {
    Header,
    Banner,
    Advantages,
    Availability,
    AboutUs,
    AboutManufacture,
    Form,
    OurPartners,
    Reviews,
    Map,
    Footer,
  },
  data() {
    return {
      reviewsData: reviewsData,
      availabilityData: availabilityData,
    };
  },
};
</script>
