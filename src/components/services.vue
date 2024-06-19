<template>
<main class="p-10 text-blue-950 scroll-m-10" id="services">
    <h2 class="text-2xl md:text-5xl text-center font-semibold">Our Services</h2>
    <div class="grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-10 mt-10">
        <section v-for="service of services" class=" rounded-xl  shadow-lg py-2 px-3 flex flex-col items-center justify-center hover:scale-105 transition-all">
           
            <h3 class="text-md my-1 font-medium">{{ service.title }}</h3>
           
        </section>
    </div>
    </main>
</template>
<script setup>
import { ref } from 'vue'
    const services = ref([
        {
            title:'CREDIT FACILITATION, DEBT RECOVERY & AGENCY BANKING'
        },
        {
            title:'TAX CONSULTING & ACCOUNTING'
        },
        {
            title:'SERVICES WITH GRANT FACILATION'
        },
        {
            title:'MANAGEMENT CONSULTANCY'
        },
        {
            title:'CREDIT AND FINANCIAL CONSULTANCY'
        },
        {
            title:'FINANCIAL INTERMEDIATION & REVENUE CONSULTANCY'
        },
        {
            title:'DEBT RESCHEDULING AND RESTRUCTURING & GENERAL SERVICES'
        },
        {
            title:'FINANCIAL ACCOUNTING, TAX AUDIT AND MANAGEMENT TRAINING'
        },
        {
            title:'PAYROLL SYSTEM MANAGEMENT AND FINTECH SOLUTION'
        },
        {
            title:'ENTREPRENEURSHIP DEVELOPMENT AND TRAINING SERVICES'
        },
    ])
</script>