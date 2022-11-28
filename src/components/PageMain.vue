<template>
  <div class="container">
    <div
      v-if="arrDischi"
      class="row row-cols-4 g-5"
    >
      <CardDisk
        v-for="dischi in arrDischi"
        :key="dischi.poster"
        :img-url="dischi.poster"
        :name="dischi.name"
        :author="dischi.autore"
        :year="dischi.anno"
      />
    </div>
    <div v-else>
      Loading ...
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import CardDisk from '@/components/CardDisk.vue';
export default {
  
  components: {
    CardDisk,
  },
  data() {
    return {
      arrDischi: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music', 
    };
  },
  created() {
    // scaricare i dati
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.arrDischi = axiosResponse.data.ressponse;
      });
  },
};
</script>

<style lang="scss" scoped>
</style>