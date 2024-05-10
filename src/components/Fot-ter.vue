<template>
    <div class="fot bg-[#141E16] md:mt-14  ">
        <div class="relative flex justify-center container ">
            <div
                class="text-center items-center bg-[#DBF1E2] shadow-sm shadow-[#DBF1E2] rounded-lg md:w-1/2   py-4 space-y-4 md:absolute -top-6 ">
                <h1 class="text-3xl font-semibold">Newsletter</h1>
                <p class="text-sm container text-gray-700"> Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Cumque,
                    repellat.</p>
                <nav class="flex space-x-2 w-full flex justify-center">
                    <InputText v-model="value2" type="text" placeholder="Enter your email adress..." />
                    <Button icon="pi pi-send" aria-label="Submit" />

                </nav>

            </div>
        </div>
        <div class="md:pt-60  border-b border-gray-400 py-6">
            <div class="md:grid grid-cols-4 gap-8 text-white container">
                <div class="space-y-4">
                    <div class="Logo flex items-center space-x-2  ">
                        <img src="/public/imgs/Screenshot_from_2024-05-01_16-19-36-removebg-preview.png" alt=""
                            class="w-10 ">
                        <h1 class="text-3xl">E-Learning</h1>
                    </div>
                    <p class="text-sm md:pl-3">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam.</p>
                    <nav class="flex space-x-5 md:pl-3  ">
                        <a href="">
                            <i class="pi pi-facebook hover:text-[#4ADE80] duration-500" style="font-size: 2rem"></i>
                        </a>
                        <a href="">
                            <i class="pi pi-twitter hover:text-[#4ADE80] duration-500" style="font-size: 2rem"></i>
                        </a>
                        <a href="">
                            <i class="pi pi-instagram hover:text-[#4ADE80] duration-500" style="font-size: 2rem"></i>
                        </a>


                    </nav>

                </div>
                <div class="space-y-4 mt-6">
                    <h1 class="text-xl text-[#4ADE80]">Company</h1>
                    <nav class="flex md:flex-col gap-4 md:space-y-2 text-sm  ">
                        <router-link to="/">
                            About
                        </router-link>
                        <router-link to="/">
                            Careers
                        </router-link>
                        <router-link to="/">
                            Mobile
                        </router-link>
                        <router-link to="/">
                            Blog
                        </router-link>
                        <router-link to="/">
                            How we work
                        </router-link>
                    </nav>
                </div>
                <div class="space-y-4 mt-6">
                    <h1 class="text-xl text-[#4ADE80]">Contact</h1>
                    <nav class="flex md:flex-col gap-4 md:space-y-2 text-sm  ">
                        <router-link to="/">
                            Help/FAQ
                        </router-link>
                        <router-link to="/">
                            Press
                        </router-link>
                        <router-link to="/">
                            Affliates
                        </router-link>
                        <router-link to="/">
                            Hotel owners
                        </router-link>
                        <router-link to="/">
                            Partners
                        </router-link>
                    </nav>
                </div>
                <div class="space-y-4 mt-6  ">
                    <h1 class="text-xl text-[#4ADE80]">More</h1>
                    <nav class="flex md:flex-col gap-2 md:space-y-2 text-sm   ">
                        <router-link to="/">
                            Airline fees
                        </router-link>
                        <router-link to="/">
                            Airlines
                        </router-link>
                        <router-link to="/">
                            Low fare tips
                        </router-link>
                        <router-link to="/">
                            Badges &
                        </router-link>
                        <router-link to="/">
                            Certificates
                        </router-link>
                    </nav>
                </div>


            </div>


        </div>
        <div class="md:px-8 px-4 flex justify-between items-center py-4 text-white">
            <h1 class="text-sm  ">&copy; 2024.E-Learning.All rights reserved</h1>
            <div class="md:flex space-x-6 hidden ">
                <h2>Privacy policy</h2>
                <h2 class="border-l pl-4 ">Terms & conditions</h2>
            </div>

        </div>
    </div>
</template>

<script setup>
import InputText from 'primevue/inputtext';
import 'primeicons/primeicons.css'
import Button from 'primevue/button';


</script>

<style scoped>
.fot {
    border-radius: 100% 0% 100% 0% / 48% 100% 0% 52%;

}
</style>