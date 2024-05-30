<script>
  import Card from "./Card.vue";
  export default {
    data() {
      return {
        photos: [
          {
            src: "./img/1.webp",
            alt: "./img/1b.webp",
            brand: "Levi's",
            text: "RELAXED FIT TEE UNISEX",
            price: 14.98,
            discount: 50,
            sustein: true,
          },
          {
            src: "./img/2.webp",
            alt: "./img/2b.webp",
            brand: "Guess",
            text: "ROSES TEE",
            price: 20.99,
            discount: 30,
            sustein: false,
          },
          {
            src: "./img/3.webp",
            alt: "./img/3b.webp",
            brand: "Come Zucchero Filato",
            text: "VOGLIA DI COLORI PASTELLO",
            price: 129.99,
            discount: 30,
            sustein: true,
          },
          {
            src: "./img/4.webp",
            alt: "./img/4b.webp",
            brand: "Levi's",
            text: "TEE UNISEX",
            price: 14.99,
            discount: 50,
            sustein: true,
          },
          {
            src: "./img/5.webp",
            alt: "./img/5b.webp",
            brand: "Maya Deluxe",
            text: "STRIPE BODICE",
            price: 99.99,
            discount: 0,
            sustein: false,
          },
          {
            src: "./img/6.webp",
            alt: "./img/6b.webp",
            brand: "Espirit",
            text: "MAGLIONE - BLACK",
            price: 29.99,
            discount: 0,
            sustein: false,
          },
        ],
      };
    },

    components: {
      Card,
    },
  };
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col" v-for="(photo, index) in photos" :key="index">
        <Card :photo="photo" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .container {
    max-width: 1200px;
    margin: 0 auto;

    .row {
      display: flex;
      flex-wrap: wrap;

      .col {
        margin: 20px;
        width: calc(100% / 3 - 40px);
      }
    }
  }
</style>
