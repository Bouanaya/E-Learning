<template>
    <div>
        <div class=" py-8 container">
            <div class="flex justify-between items-center md:container ">
                <h1 class="text-2xl md:text-5xl">Testimoni from our students</h1>
                <nav class="flex md:gap-4 gap-2">
                    <button class="rounded-full bg-primary-300 p-2" @click="myCarousel.prev()"><svg
                            xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" class="w-6 h-6 text-white hover:text-black duration-500">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M10.5 19.5 3 12m0 0 7.5-7.5M3 12h18" />
                        </svg>
                    </button>
                    <button class="rounded-full bg-primary-300 p-2" @click=" myCarousel.next()"><svg
                            xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" class="w-6 h-6 text-white hover:text-black duration-500">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
                        </svg>
                    </button>
                </nav>
            </div>
            <div class="pt-6">

                <Carousel :itemsToShow="3" :wrapAround="false" :transition="500" v-bind="settings"
                    :breakpoints="breakpoints" ref="myCarousel">
                    <Slide v-for="slide in 4" :key="slide">
                        <div class="carousel__item">
                            <div class="">
                                <div class="flex space-x-4 items-center">
                                    <img src="/public/imgs/vueschool_vuejs_bart_ledoux.jpg"
                                        class="w-14 h-14  rounded-full " alt="">
                                    <div class="px-2 ">
                                        <h1>Leslie Alexander</h1>
                                        <h1 class=" text-gray-500 text-sm text-left">CEO Porkview</h1>
                                        <nav class="flex gap-1">
                                            <img src="/public/imgs/star_77949.svg" alt="" class="w-4 h-4">
                                            <img src="/public/imgs/star_77949.svg" alt="" class="w-4 h-4">
                                            <img src="/public/imgs/star_77949.svg" alt="" class="w-4 h-4">
                                            <img src="/public/imgs/star_77949.svg" alt="" class="w-4 h-4">
                                            <img src="/public/imgs/star_77949.svg" alt="" class="w-4 h-4">

                                        </nav>
                                    </div>
                                </div>
                                <p class="text-sm text-left pt-3">Lorem ipsum dolor sit, amet consectetur adipisicing
                                    elit. Minus odio ut illo fuga.
                                    Assumenda porro, quisquam, iste, harum neque ipsum doloremque nihil nisi amet quas
                                    quo molestiae ratione dolorum itaque.</p>
                            </div>
                        </div>
                    </Slide>

                    ...
                </Carousel>
            </div>


        </div>

    </div>
</template>

<script setup>
import { Carousel, Slide } from 'vue3-carousel'
import {ref} from 'vue'

import 'vue3-carousel/dist/carousel.css'
const myCarousel = ref(null)

const settings = {
    itemsToShow: 1,
    snapAlign: 'center',
}
const breakpoints = {
    700: {
        itemsToShow: 3,
        snapAlign: 'center',
    },
    // 1024 and up
    1024: {
        itemsToShow: 3,
        snapAlign: 'center',
    },

}

</script>

<style  scoped>
.carousel__slide {
    padding: 5px;
}

.carousel__viewport {
    perspective: 2000px;
}

.carousel__track {
    transform-style: preserve-3d;
}

.carousel__slide--sliding {
    transition: 0.5s;
}

.carousel__slide {
    opacity: 0.5;
    transform: rotateY(-20deg) scale(0.9);
}

.carousel__slide--active~.carousel__slide {
    transform: rotateY(20deg) scale(0.9);
}

.carousel__slide--prev {
    opacity: 0.5;
    transform: rotateY(-10deg) scale(0.9);
}

.carousel__slide--next {
    opacity: 0.5;
    transform: rotateY(10deg) scale(0.9);
}

.carousel__slide--active {
    opacity: 1;
    transform: rotateY(0) scale(1);
}
</style>