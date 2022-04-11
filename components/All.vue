<template>
  <div class="glide relative">
    <div class="glide__track" data-glide-el="track">
      <ul class="glide__slides bg-[blue]">
        <li
          class="glide__slide flex justify-center items-center p-3 bg-[orange]"
        >
         <Card/>
        </li>
        <li
          class="glide__slide flex justify-center items-center p-3 bg-[#ff1a25]"
        >
          <Card/>
        </li>
        <li
          class="glide__slide flex justify-center items-center p-3 bg-[yellow]"
        >
          <!-- > - Move one forward <br />
          &lt; - Move one backward <br />
          ={i} - Go to zero-based {i} slide (eq. '=1', will go to second slide)
          <br />
          >> - Rewinds to the end (last slide) <br />
          &lt;&lt; - Rewinds to the start (first slide) -->
          <Card/>
        </li>
      </ul>
    </div>
    <!-- controls
  -->
    <!-- skip to the end and beginning -->
    <!-- <div data-glide-el="controls">
      <button data-glide-dir="<<">Start</button>
      <button data-glide-dir=">>">End</button>
    </div> -->
    <!-- navigation -->
    <div class="glide__arrows" data-glide-el="controls">
      <button
        class="
          glide__arrow glide__arrow--left
          !text-[#f86540]
          !bg-[black]
          !top-[-2rem]
        "
        data-glide-dir="<"
      >
        prev
      </button>
      <button
        class="
          glide__arrow glide__arrow--right
          absolute
          !text-[#f86540]
          !bg-[black]
          !top-[-2rem]
        "
        data-glide-dir=">"
      >
        next
      </button>
    </div>
    <!-- pagination -->
    <div class="glide__bullets bg-[green]" data-glide-el="controls[nav]">
      <button class="glide__bullet bg-[pink]" data-glide-dir="=0"></button>
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
    return {};
  },
  mounted() {
    if (process.browser) {
      new Glide(".glide", {
        type: "carousel",
        perView: 2,
        focusAt: 0,
        gap:40,
        // animationTimingFunc: 'bounce',
        animationDuration: 1800,
        breakpoints: {
          800: {
            perView: 2,
          },
          480: {
            perView: 1,
          },
        },
      }).mount();
    }
  },
};
</script>


<style scoped>
</style>