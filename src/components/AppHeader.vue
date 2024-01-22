<script>
export default {
  data() {
    return {
      counter: null,
      navlist: [
        {
          pageName: "CHARACTERS",
          link: "#nogo"
         
        },
        {
          pageName: "COMICS",
          link: "#nogo"
         
        },
        {
          pageName: "MOVIES",
          link: "#nogo"
         
        },
        {
          pageName: "TV",
          link: "#nogo"
         
        },
        {
          pageName: "GAMES",
          link: "#nogo"
         
        },
        {
          pageName: "COLLECTIBLES",
          link: "#nogo"
         
        },
        {
          pageName: "VIDEOS",
          link: "#nogo"
         
        },
        {
          pageName: "FANS",
          link: "#nogo"
         
        },
        {
          pageName: "NEWS",
          link: "#nogo"
         
        },
      ],
    };
  },
  methods: {
 
  },
};
</script>

<template>
  <div class="container">
    <header>
      <div class="img-box">
        <img src="/vue-dc-comics-1/img/dc-logo.png" alt="" />
      </div>
      <nav>
        <ul>
          <li 
          v-for="(elem, i) in navlist" 
           :class="{ 'active': counter == i }"
          >
            <a @click="counter = i" 
            :class="{ 'active-link': counter == i }"
            :href="elem.link">{{ elem.pageName }}</a>
          </li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/reset.scss" as *;
@use "../assets/scss/main.scss" as *;
.container {
  width: $fullSpace;
  height: $sectionHeight;
  > header {
    height: $sectionHeight;
    width: $containerSize;
    margin: 0 auto;
    display: flex;
    nav {
      flex-grow: 1;
      ul {
        display: flex;
        height: $sectionHeight;
        align-items: center;
        justify-content: end;

        li {
          list-style: none;
          margin-left: 20px;
          text-align: end;
          height: $sectionHeight;
          line-height: $sectionHeight;
          a {
            text-decoration: none;
            color: black;
            font-size: 14px;
            font-weight: 600;
          }
          &:hover {
            border-bottom: 4px solid $dc-color;
            color: $dc-color;
          }
          &:hover > a {
            color: $dc-color;
          }
        }
      }
    }
  }
  .img-box {
    width: 30%;
    height: $sectionHeight;
    display: flex;
    align-items: center;
    margin-left: 20px;
    img {
      width: 70px;
      height: 70px;
    }
  }
}


</style>
