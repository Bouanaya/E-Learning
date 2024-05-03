<template>

    <div class=" logos flex justify-center overflow-hidden z-0 ">
        <div class="flex space-x-8 logo ">
            <img src="/public/imgs/google-1-1-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            <img src="/public/imgs/linkedin-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            <img src="/public/imgs/microsoft-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            <img src="/public/imgs/slack-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            <img src="/public/imgs/xbox-one-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            <img src="/public/imgs/spotify-1-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            <img src="/public/imgs/netflix-2-logo-svgrepo-com.svg" alt="" class="w-24 md:w-32 h-32 ">
            
        </div>
    

    </div>






</template>

<script setup>

</script>

<style   scoped>
@media only screen and (max-width: 600px) {
@keyframes Slide {
        from {
            transform: translateX(0%);
        }

        to {
            transform: translateX(-100%)
        }

    }

    .logo {
        animation: 25s Slide infinite linear;



    }

    .logos:hover {
        animation-play-state: paused;
    }
}



</style>