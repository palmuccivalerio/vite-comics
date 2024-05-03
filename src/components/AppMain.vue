<script>
export default {  
  data() {
    return {
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
    <h2> -> Content goes here <-- </h2>
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