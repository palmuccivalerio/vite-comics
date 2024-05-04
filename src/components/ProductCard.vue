<script>
export default {
  props: {
    cardImage: String,
    cardTitle: String,
    cardType: String,
  },
};
</script>

<template>
  <div class="card" :class="cardType">
    <img :src="cardImage" :alt="cardTitle" />
    <p>{{ cardTitle }}</p>
  </div>
</template>

<style scoped lang="scss">

p{
  font-family: Helvetica, Arial, sans-serif;
  font-size: 10px;
}


.card {
  background-color: white;
  max-height:100px;
  max-width: 100px;

  text-align: center;
  img {
max-height: 100%;
 max-width:100%;
 
  }

}
</style>