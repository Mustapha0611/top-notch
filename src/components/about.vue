<template>
  <main class="px-10 py-10 text-blue-950" id="about">
    <h2 class="text-5xl text-center font-semibold ">About Us</h2>
    <div class="flex gap-10 justify-center mt-10 flex-wrap">
        <section v-for="about in aboutContent" class="max-w-[23rem]  rounded-xl  hover:shadow-lg p-5 flex flex-col hover:scale-105 transition-all">
            <span class="mx-auto"><img :src="about.img" class="w-20 h-20" :alt="about.title"></span>
            <h3 class="text-2xl my-5 font-medium">{{ about.title }}</h3>
            <p v-for="text in about.content">
                {{ text.subContent }}
            </p>
        </section>
    </div>
  </main>
</template>
<script setup>
import { ref } from "vue";
import img1 from "../assets/growth.png";
import img2 from "../assets/mission.png";
import img3 from "../assets/idea.png";

const aboutContent = ref([
  {
    title: "OUR VISION",
    img: img1,
    content: [
      {
        subContent:
          "Our vision is to work towards establishing a company thatprovides comprehensive financial and investment solutions that caters for the need of our diverse client base .",
      },
    ],
  },
  {
    title: "OUR MISSION",
    img: img2,
    content: [
      {
        subContent:
          "To combine strategic sales and marketing efforts with quality product offering and customer service at competitive premiums to provide the best financial solutions to all our customers and esteemed clients.",
      },
    ],
  },
  {
    title: "CORE VALUES",
    img: img3,
    content: [
      {
        subContent: "» We believe in treating our customers with respect and integrity.",
      },
      {
        subContent: "» We grow through reliability, creativity and innovation.",
      },
      {
        subContent: "» We integrate excellence and prudence in all aspects of our business.",
      },
    ],
  },
]);
</script>
