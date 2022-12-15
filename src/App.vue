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
        <div class="second-section">
          <p class="sub-heading">
            Find a Room for rent, Apartment, House, Condo, Studio, duplex, or
            shared
            <br />
            accommodation in Federal Territory of Kuala Lumpur.
          </p>
          <div class="buttons">
            <button class="btn show-btn">Show all</button>
            <button @click="prev()" class="btn arrow">
              <font-awesome-icon icon="fa-solid fa-chevron-left" />
            </button>
            <button @click="next()" class="btn arrow">
              <font-awesome-icon icon="fa-solid fa-chevron-right" />
            </button>
          </div>
        </div>
      </div>
      <div class="small-cards" id="small-cards">
        <card
          class="item"
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
          head: "Rooms1",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
        {
          head: "Studio2",
          desc: "Single room Opposite Chinatown",
          listing: "821 listings",
          img: "studio.png",
        },
        {
          head: "Apartment/condo3",
          desc: "Single room Opposite Chinatown",
          listing: "3521 listings",
          img: "apartment.png",
        },
        {
          head: "Landed House4",
          desc: "Single room Opposite Chinatown",
          listing: "1221 listings",
          img: "landedHouse.png",
        },
        {
          head: "Rooms5",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
        {
          head: "Rooms6",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
        {
          head: "Rooms7",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
        {
          head: "Rooms8",
          desc: "Single room Opposite Chinatown",
          listing: "8221 listings",
          img: "room.png",
        },
      ],
    };
  },
  methods: {
    next() {
      let section = document.getElementById("small-cards");
      let item = section.getElementsByClassName("item");
      let i = 0;
      while (i < 4) {
        section.append(item[0]);
        i++;
      }
    },
    prev() {
      let section = document.getElementById("small-cards");
      let item = section.getElementsByClassName("item");
      let i = 0;
      while (i<4) {
        section.prepend(item[item.length - 1]);
        i++;
      }
    },
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
.cards {
  margin-top: 39px;
}
.second-section {
  display: flex;
  justify-content: space-between;
}
.buttons {
  display: flex;
  /* justify-content: space-around; */
}
.buttons .btn {
  margin-top: 0px;
  margin-bottom: 0px;
  height: 35px;
  padding: 10px 10px 10px 10px;
  width: auto;
  left: 0px;
  top: 0px;
  border-radius: 100px;
  background-color: #d9d9d900;
  border: 0.5px solid #686868;
  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 16px;
}
.buttons .btn:hover {
  background-color: #d9d9d986;
}
.show-btn {
  margin-right: 44px;
}
.arrow {
  margin-right: 12px;
}
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap");
</style>
