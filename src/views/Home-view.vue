<template>
    <div class="bg-white h-screen pt-[80px]">
        <div class=" md:grid grid-cols-2  container ">
            <div class="md:pt-24 pt-12 space-y-5 ">
                <h1 class="text-5xl w-[80%]">Groz your skill to advance your career path</h1>
                <p class="">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias fugiat exercitationem ab
                    itaque soluta necessitatibus asperiores repudiandae in perspiciatis asperiores  </p>
                <Button label="Join For Free" severity="success" />
            </div>
            <div class="pt-10">
                <img src="/public/imgs/undraw_online_learning_re_qw08 (1).svg" alt="">
                 
            </div>
        </div>
    </div>

</template>
<style scoped>
h1 {
     
    background: -webkit-linear-gradient(#333, #4ADE80);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
p{
    font-family: "Poppins", sans-serif;
}
</style>
<script setup>
import Button from 'primevue/button';

</script>