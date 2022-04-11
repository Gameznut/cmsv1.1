<template>
  <div class="container relative bg-[blue]">
    <client-only>
      <swiper class="swiper" ref="mySwiper" :options="swiperOptions">
        <swiper-slide>1</swiper-slide>
        <swiper-slide>2</swiper-slide>
        <swiper-slide>3</swiper-slide>
        <swiper-slide>4</swiper-slide>
        <swiper-slide>a</swiper-slide>
        <swiper-slide>b</swiper-slide>
        <swiper-slide>c</swiper-slide>
        <swiper-slide>d</swiper-slide>
        <swiper-slide>1</swiper-slide>
        <swiper-slide>2</swiper-slide>
        <swiper-slide>3</swiper-slide>
        <swiper-slide>4</swiper-slide>
        <swiper-slide>e</swiper-slide>
        <swiper-slide>f</swiper-slide>
        <swiper-slide>g</swiper-slide>
        <swiper-slide>h</swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
    </client-only>
  </div>
</template>

<script>
export default {
  name: "carrousel",
  data() {
    return {
      swiperOptions: {
        slidesPerView: 3,
        slidesPerRow: 3,
        slidesPerColumn: 2,
        spaceBetween: 30,
        slidesPerGroup: 3,
        // grid: {
        //   fill: "column",
        //   rows: 2,
        // },
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
        // breakpoints: {
        //   900: {
        //     slidesPerView: 3,
        //     slidesPerRow: 3,
        //     slidesPerColumn: 2,
        //   },
        //   650: {
        //     slidesPerView: 2,
        //     slidesPerRow: 2,
        //     slidesPerColumn: 2,
        //     spaceBetween: 10,
        //   },
        //   0: {
        //     slidesPerView: 1,
        //     slidesPerRow: 1,
        //     slidesPerColumn: 1,
        //     spaceBetween: 10,
        //   },
        // },
      },
    };
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.$swiper;
    },
  },
  mounted() {
    this.swiper.slideTo(0, 1000, false);
    
  },
};
</script>


<style scoped>
.swiper {
  height: 440px;
  background-color: aquamarine;
  margin-left: auto;
  margin-right: auto;
}

.swiper-slide {
  background-color: red;
  height: 200px;
}
.swiper-button-prev,
.swiper-button-next {
  position: absolute;
  /* top: 0; */
}
</style>