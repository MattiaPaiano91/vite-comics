<script>
export default {
  data() {
    return {
        
    };
  },
  props: {
    image:String,
    description:String,
    comics:Object
  },
};
</script>

<template>
    
        <div class="card">
            <div class="img-box">
                <img :src="comics.thumb" :alt="comics.series">
            </div>
            <div>
                {{ comics.series }} 
            </div>
        </div>
    
</template>
<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/reset.scss" as *;

    .card{
        width: calc(100% / 6);
        height: 200px;
       .img-box{
        width: 150px;
        height: $fullSpace;
         margin: 0 auto 5px;
        
         img{
            width: 100%;
            height: 100%;
           
        }
       }
    }

</style>
