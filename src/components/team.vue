<template>
    <main class="p-10 text-blue-950" id="about">
        <h2 class="text-5xl text-center font-semibold">Our Services</h2>
        <div class="flex ">
            <section v-for="teamMember of teamMembers" class='shadow-xl border-2 rounded-md'>
                <div class="w-44 h-52">
                    <img :src="teamMember.img" class="w-full h-full" :alt="teamMember.name">
                </div>
                <p>{{ teamMember.name }} - {{ teamMember.title }}</p>
            </section>
        </div>
        </main>
    </template>
    <script setup>
    import { ref } from 'vue'
    import img1 from '../assets/ceo.jpg'
        const teamMembers = ref([
         {
            name:'Murtala lego',
            img:img1,
            title:'CEO',
            info:''
         }
        ])
    </script>