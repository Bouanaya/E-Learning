<template>
    <div class="md:flex justify-center items-center container space-x-2 space-y-8 md:space-y-0 ">
        <div class="space-y-3" v-for="{id,img,name}  in learn" :key="id">
            <div class="flex justify-center p-4">
                <img :src="img" alt="" class="w-10 h-10">
            </div>
            <h1 class="text-center font-semibold text-primary-400 text-lg">{{name}}</h1>
            <p class="text-center text-slate-600 ">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Quidem
                temporibus hic
                accusantium possimus, reprehenderit voluptatibus?</p>
            <div class="w-full flex justify-center">
                <button
                    class=" text-primary-500 border px-4 py-2 hover:bg-primary-500 hover:text-white duration-500 border-primary-500 rounded-md  ">Learn
                    More</button>
            </div>

        </div>




         
    </div>
</template>

<script setup>
const learn = [
    {
        id:0,
        img:"imgs/record-svgrepo-com.svg",
        name:"Training from expart",
        context:"",

    },
    {
        id: 1,
        img: "imgs/movie-svgrepo-com.svg",
        name: "1.5K+Vidoe course",
        context: "",

    },
    {
        id: 2,
        img: "imgs/social-contact-svgrepo-com.svg",
        name: "Occasional video update",
        context: "",

    }

]

</script>

 