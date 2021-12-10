<script>
  // Import Swiper Svelte components
  import { Swiper, SwiperSlide } from "swiper/svelte";

  // Import Swiper styles
  import "swiper/css";
</script>

<Swiper
  loop
  class="hi"
  spaceBetween={50}
  slidesPerView={3}
  on:slideChange={() => console.log("slide change")}
  on:swiper={(e) => console.log(e.detail[0])}
>
  <SwiperSlide>Slide 1</SwiperSlide>
  <SwiperSlide>Slide 2</SwiperSlide>
  <SwiperSlide>Slide 3</SwiperSlide>
  <SwiperSlide>Slide 4</SwiperSlide>
</Swiper>

<style>
  :global(.hi) {
    height: 100vh;
  }

  :global(.hi .swiper-slide) {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid red;
  }
</style>
