<template>
  <div class="container">
    <filter-btn
      v-for="(item, index) in filters"
      v-bind:key="index"
      v-bind:title="item"
    ></filter-btn>
    <div class="cards">
      <div>
        <p class="location">Malaysia > Federal Territory of Kuala Lumpur</p>
        <h1 class="heading">Federal Territory of Kuala Lumpur</h1>
        <p class="sub-heading">
          Find a Room for rent, Apartment, House, Condo, Studio, duplex, or
          shared
          <br />
          accommodation in Federal Territory of Kuala Lumpur.
        </p>
      </div>
      <div class="small-cards">
        <card
          v-for="(item, index) in cards"
          v-bind:key="index"
          v-bind:head="item.head"
          :desc="item.desc"
          :listing="item.listing"
          :img="item.img"
        ></card>
      </div>
    </div>
  </div>
</template>

<script>
import card from "./components/card.vue";
import filterBtn from "./components/elements/filterBtn.vue";
export default {
  name: "App",
  components: {
    card,
    filterBtn,
  },
  data() {
    return {
      filters: [
        "Rent",
        "Space type",
        "Zero deposit",
        "Furnishing",
        "Bath type",
        "Female only",
      ],
      cards: [
        {
          head: "Rooms",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
        {
          head: "Studio",
          desc: "Single room Opposite Chinatown",
          listing: "821 listings",
          img: "studio.png",
        },
        {
          head: "Apartment/condo",
          desc: "Single room Opposite Chinatown",
          listing: "3521 listings",
          img: "apartment.png",
        },
        {
          head: "Landed House",
          desc: "Single room Opposite Chinatown",
          listing: "1221 listings",
          img: "landedHouse.png",
        },
        {
          head: "Rooms",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
        {
          head: "Rooms",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
.container {
  padding-top: 86px;
  padding-bottom: 86px;
  padding-left: 126px;
  padding-right: 126px;
}
.small-cards {
  display: flex;
  margin-top: 39px;
  overflow-x: auto;
  scroll-behavior: smooth;
}
.small-cards::-webkit-scrollbar {
  width: 0px;
}
.heading {
  font-family: "Inter";
  font-size: 29px;
  font-weight: 600;
  line-height: 35px;
  font-style: normal;
  color: #282828;
  margin-bottom: 6px;
  margin-top: 12px;
}
.sub-heading {
  font-family: "Inter";
  font-size: 18px;
  font-weight: 300;
  line-height: 25px;
  font-style: normal;
  color: #282828;
  margin: 0px;
}
.location {
  font-family: "Inter";
  font-style: normal;
  font-weight: 300;
  font-size: 16px;
  line-height: 20px;
  color: #282828;
}
.cards{
  margin-top: 39px;
}
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap");
</style>
