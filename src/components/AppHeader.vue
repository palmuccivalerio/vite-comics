<script>
export default {
  data() {
    return {
      menu: [
        {
          title: "CHARATERS",
          isActive: false,
        },
        {
          title: "COMICS",
          isActive: true,
        },
        {
          title: "MOVIES",
          isActive: false,
        },
        {
          title: "TV",
          isActive: false,
        },
        {
          title: "GAMES",
          isActive: false,
        },
        {
          title: "COLLECTIBLES",
          isActive: true,
        },
        {
          title: "VIDEOS",
          isActive: false,
        },
        {
          title: "FANS",
          isActive: false,
        },
        {
          title: "NEWS",
          isActive: false,
        },
        {
          title: "SHOP",
          isActive: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="header-logo">
      <img
        src="../assets/img/dc-logo.png"
        alt="Logo  della DC"
       /> 
      
       <ul class="navigation">
       <li v-for="item in menu">
        <a href="" :class="{ active: item.isActive }">{{ item.title }}</a>
      </li>
    </ul>
    </div>
   
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
img{
  width:50px;
  margin-left:100px;
  margin-bottom:7px;

}

  .header-logo {
    text-align: center;
    display: flex;

  }

  ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: -2rem;
    margin-top: 10px;
    font-size:9px;
    margin-left:190px;

    a {
      padding: 8px 10px;
      text-decoration: none;
      color: $text-color;
      dispaly:flex;
      

      &:hover {
        color: $primary-dark;
      }

      &.active {
        background-color: $primary-color;
      }
    }
  }
}
</style>