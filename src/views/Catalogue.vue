<template>
  <div class="">
    <h1 class="">Catalogue</h1>
    <Search :handleSearch="handleSearch" />
    <Card :card="cardData.data" v-if="cardData.data" />
    <div class="error" v-else>
      {{cardData.error}}
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import Search from '../components/Search.vue';
import Card from '../components/Card.vue';
import API from '../API.js';

export default {
  name: 'App',
  components: {
    Search,
    Card
  },
  setup() {
    const cardData = ref({});

    const handleSearch = async (card) => {
      cardData.value = await (await fetch(`${API.BASE_URL}&fname=${card}`)).json();
    }

    return {
      handleSearch,
      cardData,
    }
  },
}
</script>

<style>
</style>
