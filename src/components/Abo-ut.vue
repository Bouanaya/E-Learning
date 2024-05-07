<template>
    <section>
        <div class=" py-10 md:py-0">
            <div class="">

                <h1 class="text-center text-3xl md:text-5xl">Trusted by 100+ Leading companies</h1>
                <Carousel />
                <div class="py-10 flex justify-center ">
                    <div class="md:w-[60%] space-y-6 container">
                        <h1 class="text-center text-3xl md:text-5xl">More than just learning</h1>
                        <p class="text-center  ">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quia
                            perspiciatis debitis voluptatibus
                            quasi asperiores libero, atque iure officiis, nisi nostrum illum </p>

                    </div>
                </div>
                <LearIng></LearIng>
               <Cours></Cours>
               <Certificat></Certificat>
               <Instructor></Instructor>

               
            </div>
        </div>
    </section>
</template>

<script setup>
import Carousel from '../components/Carousel-logo.vue'
import LearIng from './Lear-ing.vue';
import Cours from './Cou-rs.vue';
import Certificat from '../components/Certi-ficat.vue'
import Instructor from '../components/Instru-ctor.vue'
</script>

<style >
h1 , p{
    font-family: "Poppins", sans-serif;
}

</style>