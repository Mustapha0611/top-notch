<template>
  <h2 class="md:text-5xl text-3xl text-center font-semibold text-blue-950 my-5">
    Meet the team
  </h2>
  <div class="grid lg:grid-cols-4 md:grid-cols-2 sm:grid-cols-2 gap-10 p-8">
    <div
      v-for="item in items"
      :key="item.id"
      class="relative mx-auto w-72 h-80 bg-blue-300 shadow-md rounded-lg overflow-hidden"
      @mouseover="hoverItem = item.id"
      @mouseleave="hoverItem = null"
    >
      <img :src="item.img" :alt="item.name" class="h-full w-full object-fill" />
      <div
        :class="{
          'opacity-0': hoverItem !== item.id,
          'opacity-100': hoverItem === item.id,
        }"
        class="absolute cursor-pointer inset-0 bg-blue-950 bg-opacity-70 backdrop-blur-sm flex gap-4 items-center px-2 justify-center text-white text-xl flex-col transition-opacity duration-900"
      >
        <p class="text-[20px] text-center">
          {{ item.name }} <br />
          <span class="font-bold text-sm">{{ item.position }}</span>
        </p>
        <p class="text-xs leading-[1.5]">
          {{ item.text }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import img1 from "../assets/ceo.jpg";
import img2 from "../assets/ogbu.jpg";
// import img3 from "../assets/drali.jpg";
import img4 from "../assets/khalid.jpg";
import img5 from "../assets/shamsu.jpg";
const hoverItem = ref(null);
const items = ref([
  {
    id: 1,
    name: "Murtala Yusuf Fortyfour",
    position: "Ceo-MD",
    text: "The Managing Director and CEO of Topnotch Financial Services and Consulting Limited in Abuja has extensive experience in financial services and project management. He has led debt recovery and credit facilitation projects for major banks such as First Bank PLC, Access Bank PLC, and UBA. Additionally, he has collaborated with labor organizations like NULGE and SSANU. He is also a Senior Lecturer and former banker.",
    img: img1,
  },
  {
    id: 2,
    name: "Ogbu Chigozie Uwaezouke",
    position: "ACA - Director",
    text: `He is a seasoned finance professional with over 10 years of corporate experience, showcasing
exceptional initiative, team spirit, and leadership as an executive member and financial expert
consultant in the oil sector. His expertise spans accounting, bookkeeping, payroll management,
ledger management, administration, and financial analysis,
 `,   img: img2,
  },
  {
    id: 3,
    name: "Khalid Kasimu Dikko",
    position: "Director of Support Services",
    text: `Khalid is a highly experienced administrator and communication specialist with about a decade
of expertise in programme management, public relations, and strategic communications.
He has a proven track record of delivering results in complex environments. He worked with
the United Nations High Commissioner for Refugees (UNHCR) as a livelihoods facilitator in
Maiduguri, Borno State from 2016 to 2018, where he collaborated with stakeholders to enhance
the programme’s impact
`,
    img: img4,
  },
  {
    id: 4,
    name: "Shamsuddeen Haruna",
    position: "Director of Debt Recovery",
    text: `Shamsuddeen Haruna is an accomplished accountant and finance expert with extensive
experience in accounting, finance, and taxation. He brings a wealth of knowledge and expertise
to his role. Shamsuddeen has amassed considerable experience in various capacities within
the finance and accounting sectors. He works with Command Consult and Multibiz, as well
as Fourtyfour Global Concept Ltd. as a credit consultant, where he provides critical financial
insights and strategic credit solutions.
`,
    img: img5,
  },
  //   { id: 5, text: "Text for item 4", img:img5 },
  // Add more items as needed
]);
</script>

<style scoped>
/* Add any custom styles here */
</style>
