<template>
  <div :style="{ backgroundColor: 'rgb(203, 103, 13)' }" class="glide relative mb-[50px]">
    <div class="glide__track" data-glide-el="track">
      <div class="glide__slides ">
        <ul class="glide__slide grid">
          <li class="w-full p-3 ">
            <img src="../assets/images/food1.jpg" class="" alt="" />
          </li>
          <li class="w-full p-3">
            <img src="../assets/images/food1.jpg" class="" alt="" />
          </li>
        </ul>
        <ul class="glide__slide grid">
          <li class="w-full p-3">
            <img src="../assets/images/food1.jpg" class="" alt="" />
          </li>
          <li class="w-full p-3 ">
            <img src="../assets/images/food1.jpg" class="" alt="" />
          </li>
        </ul>
        <ul class="glide__slide grid">
          <li class="p-3">
            <img src="../assets/images/food2.jpg" class="test" alt="" />
          </li>
        </ul>
      </div>
    </div>

    <!-- navigation -->
    <div class="glide__arrows" data-glide-el="controls">
      <span class="glide__arrow glide__arrow--left" data-glide-dir="<">
     
        <client-only>
          <font-awesome-icon
            icon="fa-solid fa-angles-left"
            class="card_arrow"
          />
        </client-only>
      </span>
      <span
        class="glide__arrow glide__arrow--right absolute"
        data-glide-dir=">"
      >
        <client-only>
          <font-awesome-icon
            icon="fa-solid fa-angles-right"
            class="card_arrow"
          />
        </client-only>
      </span>
    </div>
    <!-- pagination -->
    <div class="glide__bullets" data-glide-el="controls[nav]">
      <button class="glide__bullet" data-glide-dir="=0"></button>
      <button class="glide__bullet" data-glide-dir="=1"></button>
      <button class="glide__bullet" data-glide-dir="=2"></button>
    </div>
  </div>
</template>

<script>
import Glide from "@glidejs/glide";
import "@glidejs/glide/dist/css/glide.core.css";
import "@glidejs/glide/dist/css/glide.theme.css";
export default {
  name: "carrousel",
  data() {
    return {
      Options: {
        type: "carousel",
        perView: 3,
        focusAt: 0,
        gap: 10,
        animationDuration: 100,
        breakpoints: {
          800: {
            perView: 2,
          },
          480: {
            perView: 1,
          },
        },
      },
    };
  },
  mounted() {
    // this.Options.perView = 1;
    const glide = new Glide(".glide", this.Options).mount();
  },
};
</script>


<style scoped>
.card {
  width: 250px;
  background-color: rgb(233, 13, 13);
}
.glide {
  /* width: 60%; */
  /* height: 400px !important; */
}

.glide__slides {
  /* width: 60% !important; */
  height: 400px;
}
.glide__slide {
  /* width: 60% !important; */
  height: 100%;
}
.grid {
  display: grid;
  row-gap: 10px !important;
}
ul li img {
  width: 100%;
  height: 170px;
  object-fit: cover;
}
.glide__arrows {
  display: flex;
  gap: 20px;
  position: absolute;
  top: -2rem;
  right: 0;
}
.glide__arrows span {
  background-color: rgb(248, 244, 2) !important;
  box-shadow: none;
  transition: 0.4s;
  color: black;
  font-size: 20px;
  border: transparent;
  outline: 0;
  position: static;
  display: block;
}

.glide__arrows span:hover {
  color: rgb(114, 111, 111);
  outline: 0;
}





.glide__bullets {
  bottom: -2rem;
}
.glide__bullet {
  background-color: black;
}
.glide__bullet--active {
  background-color: aqua;
}

/* .left,
.right {
  transition: 0.4s;
  transform: translateX(0);
}
.left:hover {
  transform: translateX(-10px);
}
.right:hover {
  transform: translateX(10px);
} */

.test {
  height: 100% !important;
}


</style>