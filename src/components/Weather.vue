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
  </div>
</template>

<script>

  import axios from 'axios';

  export default {
    name: 'Users',
    data() {
      return {
        users: null,
      };
    },
    // created: function() {
    //   axios
    //     .get('https://jsonxxxxxx')
    //     .then(res => {
    //       this.xxxxx = res.data;
    //     })
    // }
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
