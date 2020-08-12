

<template>
  <div class="container">
    <h3>NETATMO weather map widget</h3>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">City</th>
          <th scope="col">Temperature</th>
          <th scope="col">Rain</th>
          <th scope="col">Wind</th>
        </tr>
      </thead>
      <tbody>
        <!-- <tr v-for="city in cities" v-bind:key="weather.city">
          <th scope="row">Nom</th>
          <td>{{weather.temp}} °C</td>
          <td>{{weather.rain}}</td>
          <td>{{weather.wind}}</td>
        </tr> -->
      </tbody>
    </table>

    <!--Accordion wrapper-->
<div class="accordion md-accordion" id="accordionEx" role="tablist" aria-multiselectable="true">

  <!-- Accordion card -->
  <div class="card">

    <!-- Card header -->
    <div class="card-header" role="tab" id="headingOne1">
      <a data-toggle="collapse" data-parent="#accordionEx" href="#collapseOne1" aria-expanded="true"
        aria-controls="collapseOne1">
        <h5 class="mb-0">
          Paris<i class="fas fa-angle-down rotate-icon"></i>
        </h5>
      </a>
    </div>
    <!-- Card body -->
    <div id="collapseOne1" class="collapse show" role="tabpanel" aria-labelledby="headingOne1"
      data-parent="#accordionEx">
      <div class="card-body">
        <table class="table">
          <thead>
            <tr>
              <th scope="col">Temperature</th>
              <th scope="col">Rain</th>
              <th scope="col">Wind</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>°C</td>
              <td> cm</td>
              <td> km/h</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>

  </div>
  <!-- Accordion card -->

  <!-- Accordion card -->
  <div class="card">

    <!-- Card header -->
    <div class="card-header" role="tab" id="headingTwo2">
      <a class="collapsed" data-toggle="collapse" data-parent="#accordionEx" href="#collapseTwo2"
        aria-expanded="false" aria-controls="collapseTwo2">
        <h5 class="mb-0">
          Berlin<i class="fas fa-angle-down rotate-icon"></i>
        </h5>
      </a>
    </div>
    <!-- Card body -->
    <div id="collapseTwo2" class="collapse" role="tabpanel" aria-labelledby="headingTwo2"
      data-parent="#accordionEx">
      <div class="card-body">


      </div>
    </div>

  </div>
  <!-- Accordion card -->

  <!-- Accordion card -->
  <div class="card">
    <!-- Card header -->
    <div class="card-header" role="tab" id="headingThree3">
      <a class="collapsed" data-toggle="collapse" data-parent="#accordionEx" href="#collapseThree3"
        aria-expanded="false" aria-controls="collapseThree3">
        <h5 class="mb-0">
          New-York<i class="fas fa-angle-down rotate-icon"></i>
        </h5>
      </a>
    </div>
    <!-- Card body -->
    <div id="collapseThree3" class="collapse" role="tabpanel" aria-labelledby="headingThree3"
      data-parent="#accordionEx">
      <div class="card-body">


      </div>
    </div>

  </div>
  <!-- Accordion card -->
  <!-- Accordion card -->
  <div class="card">

    <!-- Card header -->
    <div class="card-header" role="tab" id="headingFour4">
      <a class="collapsed" data-toggle="collapse" data-parent="#accordionEx" href="#collapseFour4"
        aria-expanded="false" aria-controls="collapseFour4">
        <h5 class="mb-0">
          Bogota<i class="fas fa-angle-down rotate-icon"></i>
        </h5>
      </a>
    </div>
    <!-- Card body -->
    <div id="collapseFour4" class="collapse" role="tabpanel" aria-labelledby="headingFour4"
      data-parent="#accordionEx">
      <div class="card-body">


      </div>
    </div>

  </div>
  <!-- Accordion card -->

</div>
<!-- Accordion wrapper -->


  </div>
</template>

<script>

  import axios from 'axios';

  export default {
    name: 'Weather',
    data() {
      return {
        users: null,
      };
    },
    created: function() {
      axios
        .get('https://jsonxxxxxx')
        .then(res => {
          this.xxxxx = res.data;
        })
    }
  }
</script>
<style>

</style>
<!--
Paris : Latitude : 48.866667 - Longitude : 2.333333
Berlin : 52.5170365, 13.3888599
New-York : 40.7127281, -74.0060152
Bogota : 4.598481, -74.0765482
 -->
