

<template>

  <!-- Accordion card -->
  <div class="card">

    <!-- Card header -->
    <div class="card-header" role="tab" v-bind:id="collapseId + 'Heading'">
      <a data-toggle="collapse" data-parent="#accordionEx" v-bind:href="'#' + collapseId" v-bind:aria-expanded="expanded" v-bind:aria-controls="collapseId">
        <h5 class="mb-0">
          {{city}}
          <i class="fas fa-angle-down rotate-icon"></i>
        </h5>
      </a>
    </div>
    <!-- Card body -->
    <div v-bind:id="collapseId" class="collapse" role="tabpanel" v-bind:aria-labelledby="collapseId + 'Heading'"
      data-parent="#accordionEx">
      <div class="card-body">
        <table class="table">
          <thead>
            <tr>
              <th scope="col">Temperature</th>
              <!-- <th scope="col">Rain</th>
              <th scope="col">Wind</th> -->
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>{{ temperature }}°C</td>
              <!-- <td> cm</td>
              <td> km/h</td> -->
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
  <!-- Accordion card -->
</template>

<script>

  import axios from 'axios';
  export default {
    name: 'Weather',
    props: ['collapseId', 'expanded', 'city', 'coords'],

    data: function() {
      return {
        temperature: null
      }
    },

    created: function() {
      console.log(this.coords);
      let url = `https://api.netatmo.com/api/getpublicdata?lat_ne=${this.coords.lat_ne}&lon_ne=${this.coords.lon_ne}&lat_sw=${this.coords.lat_sw}&lon_sw=${this.coords.lon_sw}&filter=false`;
      let config = {
        headers: {
          Authorization: "Bearer 5f3407b3cd38442521269595|6e9028c1bf0a87435d9e453f39d5e726",
        }
      }

      axios
        .get(url, config)
        .then(res => {
          let mesure = Object.values(res.data.body[0].measures).find(measure => {return measure.type.includes("temperature")});
          let temperatureIndex = mesure.type.indexOf("temperature");
          let temperature = Object.values(mesure.res)[0][temperatureIndex];
          this.temperature = temperature;
        })
    }
  }
</script>
