<script setup>
import { ref, reactive } from "vue";
let sliderFullImageInfo = reactive({
  title: "Succulents Indoor Plant",
  desc:
    "Nature's Resilient Beauties. Succulents, a diverse group of water-storing plants, have captured the hearts of gardening enthusiasts worldwide. With their striking shapes and vibrant colors, these low-maintenance wonders thrive in arid conditions, making them perfect companions for any green space.",
  image: "https://primeslider.pro/wp-content/uploads/2022/08/1-1024x576.jpg",
});

const SliderItems = reactive([
  {
    title: "Succulents Indoor Plant",
    desc:
      "Nature's Resilient Beauties. Succulents, a diverse group of water-storing plants, have captured the hearts of gardening enthusiasts worldwide. With their striking shapes and vibrant colors, these low-maintenance wonders thrive in arid conditions, making them perfect companions for any green space.",
    image: "https://primeslider.pro/wp-content/uploads/2022/08/1-1024x576.jpg",
  },
  {
    title: "Red Potted Plan",
    desc:
      "Discovering the Charm of Succulents. Succulents, the fascinating family of plants, boast a captivating array of textures and forms. Renowned for their ability to retain water, these hardy succulents are popular choices for indoor and outdoor gardens alike, offering a delightful touch of nature to any setting.",
    image: "https://primeslider.pro/wp-content/uploads/2022/08/2.jpg",
  },
  {
    title: "Sky Blue Plant",
    desc:
      "Hardy Elegance in Greenery. Delve into the captivating world of succulents, where elegance meets resilience. Flourishing in dry climates, these adaptable plants come in an endless variety of shapes and sizes, making them perfect ornamental additions to modern interiors or enchanting outdoor landscapes.",
    image: "https://primeslider.pro/wp-content/uploads/2022/08/3.jpg",
  },
  {
    title: "Aloe Vera Plant",
    desc:
      "A Fascinating Botanical Marvel. Embark on a journey through the captivating realm of succulents, a group of plants renowned for their unique water-storing capabilities. Embracing both simplicity and sophistication, these hardy wonders effortlessly add a touch of natural beauty to homes, gardens, and spaces of all kinds.",
    image: "https://primeslider.pro/wp-content/uploads/2022/08/4.jpg",
  },
]);

function showSliderFullImageInfo(SliderItem) {
  sliderFullImageInfo.image = SliderItem.image;
  sliderFullImageInfo.title = SliderItem.title;
  sliderFullImageInfo.desc = SliderItem.desc;
}
</script>

<template>
  <h1 class="mb-5">Slider</h1>
  <div class="avatar-image flex space-x-2 w-1/4 cursor-pointer">
    <img
      v-for="SliderItem in SliderItems"
      :src="SliderItem.image"
      alt=""
      @click="showSliderFullImageInfo(SliderItem)"
    />
  </div>
  <div class="slider-image-info mt-5">
    <img :src="sliderFullImageInfo.image" alt="Slider Full Image" />
    <h2 class="text-2xl">{{ sliderFullImageInfo.title }}</h2>
    <p>{{ sliderFullImageInfo.desc }}</p>
  </div>
</template>

<style scoped></style>
