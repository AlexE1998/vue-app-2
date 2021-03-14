<template>
  <div class="home">
    <img alt="Yu-gi-oh logo" src="../assets/yugioh.png">
    <Nom msg="ERNAULT ALEXANDRE"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Nom from '@/components/contenu_accueil.vue'

export default {
  name: 'accueil',
  components: {
    Nom
  }
}
</script>
