<script>
import ProductSection from "./productSection.vue";
export default {
  data() {
    return {
      items: [
        {
          img: "/vue-dc-comics-1/img/buy-comics-digital-comics.png",
          description: "DIGITAL COMICS",
        },
        {
          img: "/vue-dc-comics-1/img/buy-comics-merchandise.png",
          description: "DC MERCHANDISE",
        },
        {
          img: "../../public/vue-dc-comics-1/img/buy-comics-subscriptions.png",
          description: "SUBSCRIPTION",
        },
        {
          img: "/vue-dc-comics-1/img/buy-comics-shop-locator.png",
          description: "COMIC SHOP LOCATOR",
        },
        {
          img: "/vue-dc-comics-1/img/buy-dc-power-visa.svg",
          description: "DC POWER VISA",
        },
      ],
      comics: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
  methods: {},
  components: {
    ProductSection,
  },
};
</script>

<template>
  <div class="container-top">
    <div class="top-main">
      <div class="jumbo-container">
        <div class="absolute-div">CURRENT SERIES</div>
      </div>
      
      <section>
        <ProductSection
          v-for="(elem, i) in comics"
          :key="i"
          :image="elem.thumb"
          :description="elem.series"
        />
      </section>
      <button>LOAD MORE</button>
    </div>
  </div>
  <div class="container-bottom">
    <div class="bottom-main">
      <section>
        <div class="img-box" v-for="(elem, i) in items" :key="i">
          <img :src="elem.img" alt="" />
          <div>
            {{ elem.description }}
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/reset.scss" as *;
.container-top {
  width: $fullSpace;

  background-color: #1c1c1c;
  .top-main {
    width: $fullSpace;
    text-align: center;
    .jumbo-container {
      width: $fullSpace;
      height: 350px;
      background-image: url("../../public/vue-dc-comics-1/img/jumbotron.jpg");
      position: relative;
        .absolute-div {
            position: absolute;
            top:96%;
            left: 20%;
            color: white;
            width:200px;
            height: 30px;
            line-height: 30px;
            font-size: 1rem;
            background-color: $dc-color;
        }
    }
    section {
      height: 600px;
      width: $containerSize;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      color: white;
      text-transform: uppercase;
      font-size: 13px;
      margin: 0 auto;
    }

    button {
      margin: 20px auto 20px;
      width: 180px;
      height: 30px;
      background-color: $dc-color;
      color: white;
      font-weight: 500;
      border: none;
      cursor: pointer;
    }
  }
}
.container-bottom {
  background-color: $dc-color;
  position: relative;
  
  .bottom-main {
    width: $containerSize;
    margin: 0 auto;
    section {
      width: $fullSpace;
      height: $sectionHeight;
      display: flex;
      color: white;
      .img-box {
        width: calc(100% / 5);
        margin-left: 20px;
        display: flex;
        align-items: center;
        img {
          width: 50px;
          margin-right: 10px;
        }
      }
    }
  }
}
</style>
