<template>
    <nav class=" fixed w-full bg-white z-50">

        <div class="  flex justify-between items-center  rounded-lg mt-2 container ">
            <div class="Logo flex items-center space-x-2  ">
                <img src="/public/imgs/Screenshot_from_2024-05-01_16-19-36-removebg-preview.png" alt="" class="w-10 ">
                <h1 class="text-3xl">E-Learning</h1>
            </div>
            <Navigation></Navigation>
            <div class="md:flex hidden space-x-6  ">

                <Button label="Sign In" severity="success" />
                <Button label="Free Trial" style="color: white;" />

            </div>
            <div class="md:hidden flex" @click="showM">
                <svg v-show="!ShowMenu" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                    stroke-width="1.5" stroke="currentColor" class="w-8 h-8 ">
                    <path stroke-linecap="round" stroke-linejoin="round"
                        d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                </svg>
                <svg v-show="ShowMenu" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                    stroke-width="1.5" stroke="currentColor" class="w-8 h-8">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
                </svg>



            </div>
        </div>
        <div class="h-2 bg-primary-50 blur-sm duration-500 w-full " v-if="Shadow">

        </div>
        <div class="absolute  -right-[200%] w-screen flex justify-end h-screen duration-1000    md:hidden z-50  "
            :class="{ ShowMen: ShowMenu }" @click.stop="showM">
            <div class="w-screen">
                <div class="flex justify-end">
                    <ul
                        class=" space-y-6 bg-primary-300  w- px-8 py-4 z-50 rounded-tl-lg rounded-bl-lg flex justify-center flex-col items-center ">
                        <li class="">
                            <router-link to="/" class="text-lg font-semibold ">About</router-link>
                        </li>
                        <li>
                            <router-link to="/" class="text-lg font-semibold">Features</router-link>
                        </li>
                        <li>
                            <router-link to="/" class="text-lg font-semibold">Pricing</router-link>
                        </li>
                        <li>
                            <router-link to="/" class="text-lg font-semibold">Testimonial</router-link>
                        </li>
                        <li>
                            <router-link to="/" class="text-lg font-semibold">Contact</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </nav>



</template>
<style scoped>
h1 {
    font-family: " Poppins", sans-serif;
}

.show {
    background-color: rgb(236 253 245);
    transition-duration: 0.5s;
}

.ShowMen {
    left: 0;
    transition-duration: 5s;
}
</style>

<script setup>
import Navigation from '../components/Navi-gation.vue'
import { ref } from 'vue'
import Button from 'primevue/button';


const Shadow = ref(false);
const ShowMenu = ref(false);
const showM = () => {
    ShowMenu.value = !ShowMenu.value
}
document.addEventListener("scroll", () => {
    let bodyPostionTop = document.body.getBoundingClientRect().top;
    if (bodyPostionTop < -100) {
        Shadow.value = true;

    } else {

        Shadow.value = false;
    }
});

</script>
