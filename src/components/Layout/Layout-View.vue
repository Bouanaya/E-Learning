<template>
    <div>
        <NavBar></NavBar>
       
            <router-view></router-view>

            <Footer></Footer>

       
    </div>
</template>

 
 <script setup>
import NavBar from '../Nav-bar.vue';
import Footer from '../Fot-ter.vue';


</script>

 