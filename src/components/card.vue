<template>
  <div class="card">
    <img class="card-img" :src="img" alt="" />
    <h5 class="title head">{{head}}</h5>
    <p class="title desc">{{desc}}</p>
    <p class="title listing">{{listing}}</p>
  </div>
</template>

<script>
export default {
  name: "card",
  props:{
    head:String,
    desc:String,
    listing:String,
    img:String,
  }
};
</script>

<style scoped>
.card {
  min-width: 256px;
  height: 372px;
  border: solid 91ack 1px;
  overflow: hidden;
  margin-right: 19px;
  border-radius: 8px;
}
.card-img {
  width: 256px;
  height: 256px;
}
.title {
  margin: 0px;
  font-size: 19.2px;
  color: #282828;
  font-family: "Inter";
}
.desc{
    font-size:16px ;
    font-weight: 300;
    line-height: 20px;
}
.listing{
    font-size:13.33px ;
    font-weight: 300;
    line-height: 17px;
}
</style>