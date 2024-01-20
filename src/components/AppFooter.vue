<script>
export default {
  data() {
    return {
      footerImg: [
        {
          img: "public/vue-dc-comics-1/img/footer-facebook.png",
        },
        {
          img: "public/vue-dc-comics-1/img/footer-periscope.png",
        },
        {
          img: "public/vue-dc-comics-1/img/footer-pinterest.png",
        },
        {
          img: "public/vue-dc-comics-1/img/footer-twitter.png",
        },
        {
          img: "public/vue-dc-comics-1/img/footer-youtube.png",
        },
      ],
    };
  },
};
</script>

<template>
 
    <footer>
      <div class="footer-top">
        <div class="col-footer">
          <h2>DC COMICS</h2>
          <ul>
            <li>Characters</li>
            <li>Comics</li>
            <li>Movies</li>
            <li>TV</li>
            <li>Games</li>
            <li>Videos</li>
            <li>News</li>
          </ul>
          <h2>SHOP</h2>
          <ul>
            <li>Shop DC</li>
            <li>Shop DC Collectibles</li>
          </ul>
        </div>
        <div class="col-footer">
          <h2>DC</h2>
          <ul>
            <li>lorem</li>
            <li>Lorem, ipsum dolor.</li>
            <li>Lorem, ipsum.</li>
            <li>lore</li>
            <li>Lorem ipsum dolor sit.</li>
            <li>Lorem ipsum dolor sit amet.</li>
            <li>lorem</li>
            <li>Lorem, ipsum.</li>
            <li>Lorem ipsum dolor sit.</li>
            <li>Lorem ipsum dolor sit amet.</li>
            <li>lorem</li>
          </ul>
        </div>
        <div class="col-footer">
          <h2>SITES</h2>
          <ul>
            <li>DC</li>
            <li>MAD Magasine</li>
            <li>DC Kids</li>
            <li>DC Universe</li>
            <li>DC Power Visa</li>
          </ul>
        </div>
        <div class="col-footer-img">
          <img src="../../public/vue-dc-comics-1/img/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </footer>
    <div class="container">
      <div class="footer-bottom">
        <div>
          <button>SIGN UP NOW!</button>
        </div>
        <div>
          <ul>
            <li>
              <h2>follow us</h2>
            </li>
            <li v-for="(elem, i) in footerImg" :key="i">
              <img :src="elem.img" alt="" />
            </li>
          </ul>
        </div>
      </div>
    </div>
 
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/reset.scss" as *;

footer {
  width: $fullSpace;
  height: 300px;
  background-image: url("/vue-dc-comics-1/img/footer-bg.jpg");
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
  h2 {
    color: white;
    margin-top: 30px;
  }
  li {
    list-style: none;
    color: gray;
  }
  .footer-top {
    width: $containerSize;
    margin: 0 auto;
    display: flex;
    height: $sectionHeight;
    .col-footer {
      margin-right: 60px;
    }
    .col-footer-img {
      overflow: hidden;
      height: 300px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-left: 100px;
      img {
        height: 150%;
      }
    }
  }
}
.container {
  width: $fullSpace;
  height: calc(100vh - 750px);
  background-color: $footer-color;
  .footer-bottom {
    width: $containerSize;
    height: $sectionHeight;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    button {
      width: 170px;
      height: 50px;
      border: 3px solid $dc-color;
      background-color: $footer-color;
      color: white;
      font-size: large;
      cursor: pointer;
    }
    ul {
      display: flex;
      align-items: center;
      justify-content: end;
    }
    li {
      list-style: none;
      margin-left: 20px;
    }
    &:nth-child(2) {
      display: flex;
      justify-content: end;
    }
    h2 {
      text-transform: uppercase;
      color: $dc-color;
    }
  }
}
</style>
