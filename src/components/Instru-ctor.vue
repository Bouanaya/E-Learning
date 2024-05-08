<template>
    <div class=" pt-8 container">
        <div class="flex justify-between items-center ">
            <h1 class="text-2xl md:text-5xl">Meet our instructor</h1>
            <nav class="flex md:gap-4 gap-2">
                <button class="rounded-full bg-primary-300 p-2" @click="myCarousel.prev()"><svg
                        xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-6 h-6 text-white hover:text-black duration-500">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 19.5 3 12m0 0 7.5-7.5M3 12h18" />
                    </svg>
                </button>
                <button class="rounded-full bg-primary-300 p-2" @click=" myCarousel.next()"><svg
                        xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-6 h-6 text-white hover:text-black duration-500">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
                    </svg>
                </button>
            </nav>
        </div>
        <div class="">
            <Carousel v-bind="settings" :breakpoints="breakpoints" ref="myCarousel">

                <Slide v-for=" {id , name ,color,img} in data" :key="id">
                    <div class="flex flex-col py-6">
                        <div class="rounded-t-full    flex justify-center   " :style="{backgroundColor: color}">
                            <img :src="img" alt="" class="">

                        </div>
                        <div class="text-center py-2">
                            <h1 class="md:text-2xl text-xl">{{name}}</h1>
                            <p class="text-gray-500 text-sm">Senior UX Designer</p>
                        </div>



                    </div>
                </Slide>


            </Carousel>
        </div>


    </div>



</template>
 
<script setup>
 
import { Carousel, Slide } from 'vue3-carousel'


import 'vue3-carousel/dist/carousel.css'

import { ref } from 'vue'


const data =[
    {
        id :0,
        img:"/imgs/Screenshot_from_2024-05-07_17-54-17-removebg-preview.png",
        name:"Leslie Alexander",
        color:"#A9FFFE"
    },
    {
        id: 1,
        img: "/imgs/Screenshot_from_2024-05-07_17-54-25-removebg-preview.png",
        name: "Wade Warren",
        color: "#d3f6de"
    },
    {
        id: 2,
        img: "/imgs/Screenshot_from_2024-05-07_17-54-37-removebg-preview.png",
        name: "Annette Black",
        color: "#d5d9ff"
    },
    {
        id: 3,
        img: "imgs/Screenshot_from_2024-05-07_17-54-48-removebg-preview.png",
        name: "Floyd Miles",
        color: "#ffe3c3"
    },
    {
        id: 4,
        img: "imgs/Screenshot_from_2024-05-07_17-54-48-removebg-preview.png",
        name: "Floyd Miles",
        color: "#ffe3c3"
    },



]

const myCarousel = ref(null)

const settings = {
    itemsToShow: 2,
    snapAlign: 'center',
}
const breakpoints = {
    700: {
        itemsToShow: 3.5,
        snapAlign: 'center',
    },
    // 1024 and up
    1024: {
        itemsToShow: 4,
        snapAlign: 'center',
    },

}



</script>
<style>
 .carousel__track {
    gap: 20px;
    
    

}


</style>