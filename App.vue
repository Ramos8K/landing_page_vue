<script setup>
import HeaderView from "./components/HeaderView.vue";
import Section1 from "./components/Section1.vue";
import Section2 from "./components/Section2.vue";
import Section3 from "./components/Section3.vue";
import Carousel from "primevue/carousel";
import { ProductService } from "./service/ProductService";
import Section4 from "./components/Section4.vue"
</script>

<template>
  <HeaderView />
  <Section1 />
  <Section2 />
  <div class="lg:h-section3-desktop sm:h-section3-mobile md:h-section3-tablet h-section4-minimobile" id="section2" >
    <div class="container mx-auto text-center md:text-start max-w-screen-2xl">
      <div class="flex flex-col items-center pb-16">
        <div class="text-center max-w-screen-md pt-20 space-y-4">
          <h1 class="md:text-primary md:text-3xl text-primary text-xl">
            O QUE VOCÊ IRÁ APRENDER
          </h1>
        </div>
      </div>
      <div class="card">
        <Carousel
          :value="products"
          :numVisible="3"
          :numScroll="3"
          :responsiveOptions="responsiveOptions"
        >
          <template #item="slotProps">
            <div
              class="border border-surface-500 dark:border-surface-700 rounded m-2"
            >
              <div class="mb-4">
                <div class="relative mx-auto">
                  <img :src="'/src/assets/banner.png'" class="w-full rounded" />
                  <Tag
                    :value="slotProps.data.inventoryStatus"
                    :severity="getSeverity(slotProps.data.inventoryStatus)"
                    class="absolute"
                    style="left: 5px; top: 5px"
                  />
                </div>
              </div>
              <div class="mb-4 font-medium text-center text-primary">{{ slotProps.data.name }}</div>
              
            </div>
          </template>
        </Carousel>
      </div>
      <Section3/>
    </div>
  </div>
  <Section4/>
</template>

<script>
export default {
  data() {
    return {
      products: null,
      responsiveOptions: [
        {
          breakpoint: "1400px",
          numVisible: 2,
          numScroll: 1,
        },
        {
          breakpoint: "1199px",
          numVisible: 3,
          numScroll: 1,
        },
        {
          breakpoint: "767px",
          numVisible: 2,
          numScroll: 1,
        },
        {
          breakpoint: "575px",
          numVisible: 1,
          numScroll: 1,
        },
      ],
    };
  },
  mounted() {
    ProductService.getProductsSmall().then(
      (data) => (this.products = data.slice(0, 9))
    );
  },
  methods: {
    getSeverity(status) {
      switch (status) {
        case "INSTOCK":
          return "success";

        case "LOWSTOCK":
          return "warn";

        case "OUTOFSTOCK":
          return "danger";

        default:
          return null;
      }
    },
  },
};
</script>

<style scoped>
#section2 {
    background-image: url("/src/assets/section-2.png") ;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
</style>
