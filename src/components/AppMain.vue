<script>

import { productsArray } from "../assets/data/dc-comics.js";
import ProductCard from "./ProductCard.vue";

export default { 
  components: {
    ProductCard
  },
  data() {
    return {
      products: productsArray,
      menu: [
        {
          title: "DIGITAL COMICS",
          isActive: false,
        },
        {
          title: "DC MERCHANDISE",
          isActive: true,
        },
        {
          title: "SUBSCRIPTION",
          isActive: false,
        },
        {
          title: "COMIC SHOP LOCATOR",
          isActive: false,
        },
        {
          title: "DC POWER VISA",
          isActive: false,
        },
  
      ],
    };
  },};
</script>

<template>
  <section class="products">

<div class="row">
  <div class="col" v-for="prod in products">
    <ProductCard
      :cardImage="prod.thumb"
      :cardTitle="prod.series"
      :cardType="prod.type"
    />
  </div>
</div>
  </section>

 <section>
  <ul class="digi-navigation">
      <li v-for="item in menu">
        <a href="" :class="{ active: item.isActive }">{{ item.title }}</a>
      </li>
    </ul>
 </section>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;

h2{
  text-align: left;
}


section {
  background-color: black;
  
}
.products {
  margin-top: 0rem;
  padding: 3rem 0;
  color:white;
 

 

  @include flex(row, center, center);
}



.row {
    @include flex(row, space-between, wrap);


    .col {
      width: 50%;
      margin-top:10rem;
      margin-bottom: 10rem;
    }
  }





ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 1rem;
    margin-top: 0px;
}

    a {
      padding: 8px 10px;
      text-decoration: none;
     
      dispaly:flex;
    }



</style>