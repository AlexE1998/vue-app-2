<template>
  <div class="card">
    <span class="favorite"></span>
    <h2>{{card[0].name}}</h2>

    <div class="card_details">
      <div class="card_detailsLeft">
        <img :src="card[0].card_images[0].image_url" />
      </div>
      <div class="card_detailsRight">
        <div class="card_detailsRight">
         <h4>Type:</h4> {{card[0].type}}
        </div>
        <div class="card_detailsRight">
          <h4>Description:</h4> {{card[0].desc}}
        </div>
        <div class="card_detailsRight">
          <h4>Attaque:</h4> {{card[0].atk}}
        </div>
        <div class="card_detailsRight">
          <h4>Defense:</h4> {{card[0].def}}
        </div>
        <div class="card_detailsRight">
          <h4>Niveau:</h4> {{card[0].level}}
          <img
              src="https://ygoprodeck.com/wp-content/uploads/2017/01/level.png"
              width="20"
              height="20"
            />
        </div>
        <div class="card_detailsRight">
          <h4>Race:</h4> {{card[0].race}}
        </div>
        <div class="card_detailsRight">
          <h4>Attribut:</h4> {{card[0].attribute}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    card: Object,
  },
}
</script>
