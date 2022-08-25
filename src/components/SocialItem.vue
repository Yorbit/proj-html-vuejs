<template>
  <section class="SocialImg">
    <img :src="require('../assets/img/'+image)" :alt="titleAlt" />
  </section>
</template>

<script>
export default {
    props:{
        'image': String,
        'titleAlt': String,
    }
};
</script>

<style scoped lang="scss">
.SocialImg{
    margin-bottom: 30px;
    width: calc(100% / 4 - 14px);
    line-height: 0;
        img{
            width: 100%;
        }
}
.SocialImg:nth-child(1){
  margin-right: 28rem;
}
</style>