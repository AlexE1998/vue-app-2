<template>
  <form class="searchForm" @submit.prevent="handleSubmit">
    <label for="cardName">Rentrez le nom de la carte : </label>
    <input type="text" id="cardName" v-model="cardName" />
    <button type="submit">Chercher</button>
  </form>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Search',
  props: {
    handleSearch: Function,
  },
  setup(props) {
    const cardName = ref('Dragon Blanc aux Yeux bleus');

    const handleSubmit = () => {
      props.handleSearch(cardName.value);
    };

    return {
      cardName,
      handleSubmit,
    };
  },
}
</script>
