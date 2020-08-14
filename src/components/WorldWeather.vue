<template>

  <div class="container">
    <h3><i class="fas fa-sun"></i> NETATMO weather map widget <i class="fas fa-cloud"></i></h3>

    <!--Accordion wrapper-->
    <div class="accordion md-accordion" id="accordionEx" role="tablist" aria-multiselectable="true">
      <Weather collapse-id="collapseOne" expanded="true" city="Paris" v-bind:coords="{lat_ne:'48.86471476180278', lon_ne:'2.373046875', lat_sw:'48.83579746243092', lon_sw:'2.3291015625'}"></Weather>
      <Weather collapse-id="collapseTwo" expanded="false" city="Berlin" v-bind:coords="{lat_ne:'52.3755991766591', lon_ne:'13.7109375', lat_sw:'52.26815737376817', lon_sw:'13.53515625'}"></Weather>
      <Weather collapse-id="collapseThree" expanded="false" city="New-York" v-bind:coords="{lat_ne:'40.97989806962013', lon_ne:'-81.5625', lat_sw:'38.82259097617712', lon_sw:'-81.5625'}"></Weather>
      <Weather collapse-id="collapseFour" expanded="false" city="Bogota" v-bind:coords="{lat_ne:'5.266007882805492', lon_ne:'-75.234375', lat_sw:'4.915832801313174', lon_sw:'-75.5859375'}"></Weather>
    </div>
    <!-- Accordion wrapper -->

  </div>
</template>

<script>
import Weather from './Weather.vue'
export default {
  name: 'WorldWeather',
  components: {
    Weather
  }
}
</script>

<style>

  .accordion {
    margin: auto;
    width: 40vw;
  }

  h3 {
    margin-bottom: 5rem;
  }

  i {
    color: #007bff;
  }

</style>
