<template>
  <div class="home">
      <NavBar/>
      <div class="container">
        <HeroPage/>
        <div class="row mt-4">
          <div class="col">
            <h3>Paket Wisata Terbaik Untukmu</h3>
          </div>
          <div class="col">
            <router-link to="/wisataterbaik" class="btn btn-secondary float-end"><b-icon-eye></b-icon-eye> Lihat Semua</router-link>
          </div>
        </div>

        <div class="row mb-">
          <div class="col-md-4 mt-4" v-for="paketwisata in wisata" :key="paketwisata.id">
            <CardPage :paketwisata="paketwisata"/>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src

import NavBar from '@/components/NavBar.vue'
import HeroPage from '@/components/HeroPage.vue'
import CardPage from '@/components/CardPage.vue'
import axios from "axios"

export default {
  name: 'HomeView',
  components: {
    NavBar,
    HeroPage,
    CardPage
  },
  data() {
    return{
      wisata: []
    }
  },
  methods: {
    setWisata(data) {
      this.wisata = data
    }
  },
  mounted() {
    axios.get('http://localhost:3000/wisata-terbaik')
    .then((response) => this.setWisata(response.data))
    .catch((error) => console.log(error))

  }
}
</script>
