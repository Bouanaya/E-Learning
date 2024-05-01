<template>

    <nav class=" fixed w-full bg-transparent  ">
        <div class="  flex justify-between items-center duration-500 rounded-lg   mt-2  container "
            :class="({ show:MenuShow })">
            <div class="Logo flex items-center  ">
                <img src="/public/imgs/Screenshot_from_2024-05-01_16-19-36-removebg-preview.png" alt="" class="w-14 ">
                <h1 class="text-3xl">E-Learning</h1>
            </div>
            <Navigation></Navigation>
            <div class="flex space-x-6  ">

                <Button label="Sign In" severity="success" />
                <Button label="Free Trial" style="color: white;" />

            </div>
        </div>
    </nav>



</template>
<style scoped>
h1 {
    font-family: " Poppins", sans-serif;
}
.show{
    background-color:rgb(236 253 245) ;
     
        transition-duration: 0.5s;
}
</style>

<script setup>
import Navigation from '../components/Navi-gation.vue'
import { ref } from 'vue'
import Button from 'primevue/button';


const MenuShow = ref(false);
document.addEventListener("scroll", () => {
    let bodyPostionTop = document.body.getBoundingClientRect().top;
    if (bodyPostionTop < -100) {
        MenuShow.value = true;

    } else {

        MenuShow.value = false;
    }
});

</script>
