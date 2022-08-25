<template>
    <div class="zone_location">
        <div class="zone_img">
            <img :src="require('../assets/img/'+image)" alt="">
        </div>
        <div class="info_location">
            <h1 class="title"> {{ country }} </h1>
            <ul class="infoSpan">
                <li>CALL US<span> {{ phone }} </span></li>
                <li>OPEN ALL WEEK<span> {{ hours }} </span></li>
                <li><button class="btn light">View Map</button></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        'image': String,
        'country': String,
        'hours': String,
        'phone': String,
    }
};
</script>

<style scoped lang="scss">
@import "../styles/generals.scss";

.zone_location:nth-child(1) .info_location{
  background-color: rgba($Atoll, 0.1);
}
.zone_location {
  width: 50%;
}
.zone_img{
  line-height: 0;
}
.zone_img img{
  width: 100%;
}
.title{
  font-size: 1.6rem;
}
.info_location {
  background-color: rgba($Chalky, 0.3);
  padding: 40px 0px;
  text-align: center;
}
span {
  display: block;
}
.infoSpan {
  display: flex;
  justify-content: space-around;
  list-style: none;
  padding-top: 20px;
  align-items: center;
  li {
    color: $Mamba;
    line-height: 30px;
    font-size: 14px;
    font-weight: 500;
  }
}
</style>