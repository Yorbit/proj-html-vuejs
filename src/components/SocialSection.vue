<template>
  <div id="socialShots" class="container">
    <div class="zoneSocialItem flex between">
        <SocialItem v-for="(element, index) in socialItem"
        :key="index"
        :image="element.img"
        :titleAlt="element.titleAlt"/>
    </div>
    <div class="socialMore">
        <div>
            <h6 class="philosophy">MADE FOR SHARING</h6>
            <h1 class="title">Let's stay in touch</h1>
            <button class="btn dark"><i class="fa-brands fa-instagram"></i>Follow us</button>
        </div>
    </div> 
  </div>
</template>

<script>
import SocialItem from './SocialItem.vue';
export default {
    components:{
        SocialItem,
    },
    data: function () {
    return {
      socialItem: [
        {
          img: "social-1.jpg",
          titleAlt: "social-1.jpg",
        },
        {
          img: "social-2.jpg",
          titleAlt: "social-2.jpg",
        },
        {
          img: "social-3.jpg",
          titleAlt: "social-3.jpg",
        },
        {
          img: "social-5.jpg",
          titleAlt: "social-5.jpg",
        },
        {
          img: "social-4.jpg",
          titleAlt: "social-4.jpg",
        },
        {
          img: "social-6.jpg",
          titleAlt: "social-6.jpg",
        },
      ],
    };
  },
}
</script>

<style scoped lang="scss">
@import "../styles/generals.scss";
.container{
    position: relative;
}
.zoneSocialItem{
    flex-wrap: wrap;
    position: relative;
}

.socialMore{
    width: calc(100% / 2 - -30px);
    height: 374px;
    width: 790px;
    background-color: rgba($Perfume, 0.1);
    position: absolute;
    bottom: 27.2rem;
    right: 25.4rem;
    text-align: center;
    div{
        margin-top: 7rem;

        i{
            padding-right: 5px;
        }
        h6{
            font-size: 10px;
            font-weight: 400;
            padding-bottom: 20px;
        }
    }
}
</style>