<template>
    <div class="container">
        <input type="text" v-model="keyword" />
        <button @click="searchData()">Search Anime</button>
        <!-- {{resultData}} -->

    <div v-for="data in resultData" :key="data.name">
        <!-- ID = {{data.mal_id}}
        Name = {{data.title}}
        Detail = {{data.synopsis}}
        Image = {{data.image_url}} -->

<b-card-group columns >
    <b-card v-for="data in resultData" :key="data.name"
    :title="data.deaths"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <b-card-text>
      <!-- {{data.synopsis}} -->
        {{data.name}}
        {{data.total_cases}}
        {{data.deaths}}
    </b-card-text>

    <!-- <b-button href="#" variant="primary">Go somewhere</b-button> -->
  </b-card>
</b-card-group>

    </div>

    </div>
</template>


<script>
import Axios from 'axios'
export default {
    data(){
        return{
            resultData:null,
            keyword:''
        }
    },

    methods:{
        searchData(){
            console.log('searchData');
          Axios
            .get('https://api.quarantine.country/api/v1/spots/region?region=+'+this.keyword+'&page=1')
            .then( (response) => {
                this.resultData = response.data.results
            })
            .catch((err) => {
                console.log(err)
            })
        },
    },
}
</script>


<style>

</style>