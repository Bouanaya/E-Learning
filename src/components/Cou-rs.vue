<template>
    <div class="bg-primary-200 mt-5 cours">
        <div class="py-14 container ">
            <div class="flex justify-between items-center">
                <h1 class=" text-3xl md:text-5xl">Most Popular Courses</h1>
                <button class="flex items-center text-primary-400 md:text-lg text-sm  "><span
                        class="md:flex hidden">Explore
                        courses</span> <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                        stroke-width="1.5" stroke="currentColor" class="w-8 md:hidden flex">
                        <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
                    </svg>
                </button>
            </div>
      <BoxLearn/>
        </div>
    </div>
</template>

<script setup>
import BoxLearn from '../components/Box-learn.vue'

</script>

<style  scoped>
.cours{
    border-radius:0% 100% 0% 100% / 0% 100% 0% 100%;
}

</style>